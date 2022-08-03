<script lang='ts'>
import Article from './Article.svelte';
import GameHistory from './GameHistory.svelte';
import type { Client } from 'tmi.js';
import twitch from 'tmi.js';

const tw_channel = get_twitch_connection('femeuc');
tw_channel.on('message', (channel, tags, message, self) => {

});

function get_twitch_connection( channel_name: string ): Client {
    const client = new twitch.Client({
        channels: [ channel_name ]
    });
    client.connect();
    return client;
}
</script>

<div class="index">
    <div class="wrapper">
    <Article />
    </div>
    <div class="wrapper">
    <GameHistory />
    </div>
</div>

<style>
    :root {
        --body-bg-color: hsl(0, 0%, 0%);
        --text-color: hsl(0, 50%, 100%);
        --font-size: calc(12px + 1vw);
        --content-pad: 10px;
    }
    :global(*) {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    :global(body) {
        background-color: var(--body-bg-color);
        color: var(--text-color);
        overflow: auto hidden;
        min-width: 900px;
        font-size: var(--font-size);
    }
    .index {
        display: grid;
        grid-template-columns: 6fr 3fr;
        grid-template-rows: 95vh;
        padding: var(--content-pad);
    }
    .index .wrapper {
        padding: var(--content-pad);
        overflow-y: auto;
    }
</style>