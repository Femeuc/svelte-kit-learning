<script lang='ts'>
    export let word_to_be_highlighted: string = '';

    let ul: HTMLElement;

    export function add_player_hunch(player_name: string, hunch: string, ocurrences: number): void {
        const li = document.createElement('LI');
        li.onmousemove = () => word_to_be_highlighted = hunch;
        li.innerHTML = `
            <span>${player_name}</span>
            <span>${hunch}</span>
            <span>${ocurrences}</span>
        `;
        ul?.appendChild(li);
    }
</script>

<div class="game_history">
    <h2>Game History</h2>
    <ul bind:this={ul}>
        <li class="heading">
            <span>Jogador</span>
            <span>Palavra</span>
            <span>Ocorrências</span>
        </li>
    </ul>
</div>

<style>
    :global(.game_history li) {
        display: flex;
        cursor: pointer;
    }
    :global(.game_history li:hover ) {
        background-color: rgba(255, 255, 255, 0.3);
        font-weight: bold;
    }
    :global(.game_history li span:nth-child(1)) {
        width: 35%;
    }
    :global(.game_history li span:nth-child(2)) {
        width: 45%;
    }
    :global(.game_history li span:nth-child(3)) {
        width: 20%;
    }
    :global(.game_history li.heading) { margin: 5px auto 15px auto; }
    :global(.game_history li.heading > span) {
        width: 100%;
        font-weight: bold;
    }
</style>