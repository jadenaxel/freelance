<script>
    export let settingPostIcon, settingPostTitle, settingPostQuantity;
</script>

<div class="settingsPost">
    <img src={settingPostIcon} alt="Icon" />
    <p class="title">{settingPostTitle}</p>
    {#if settingPostQuantity > 0}
        <p class="quantity">{settingPostQuantity}</p>
    {/if}
</div>

<style>
    .settingsPost {
        display: flex;
        align-items: center;
        margin-bottom: 20px;
    }
    .settingsPost:last-child {
        margin-bottom: 0;
    }
    img {
        margin-right: 10px;
    }
    .title {
        margin-right: 7px;
    }
    .quantity {
        width: 35px;
        height: 22px;
        display: flex;
        justify-content: center;
        align-items: center;
        border: 1px solid #d4d4d4;
        border-radius: 11px;
    }
</style>
