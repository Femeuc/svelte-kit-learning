<script lang="ts">
    import Input from './Input.svelte';

    let count: any = 0;

    const increment_by_one = () => {
        count++;
    }
</script>

<div class="index">
    <Input />
    <h2 on:click={increment_by_one}>Count: <span bind:innerHTML={count} contenteditable="true"></span></h2>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima unde magnam voluptatum omnis neque, cum, officiis dolor debitis tenetur natus veritatis reiciendis. Modi officia, laboriosam blanditiis exercitationem cupiditate reiciendis officiis.</p>
</div>

<style>
    .index {
        text-align: center;
        margin: 20px auto;
    }
</style>