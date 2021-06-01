<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
    const onShareClick = () => {
        dispatch("onshareClick");
    };
</script>

<div class="share-area">
    <h3 class="share-desc">liked the Meme? You can copy and share it,</h3>
    <button class="btn btn-share" on:click={onShareClick}>Share</button>
</div>

<style>
    .share-area {
        position: absolute;
        bottom: 12vh;
        max-width: 240px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .share-desc {
        flex-basis: 70%;
        padding: 5px;
        margin: 5px;
    }
    .btn-share {
        padding: 5px;
        margin: 5px;
        border-radius: 15px;
        text-align: center;
        max-width: 250px;
        outline: none;
        border: none;
        flex-basis: 20%;
    }
</style>
