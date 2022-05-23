<script>
    export let imageIconSettings, textIconSettings;
</script>

<div class="iconsContainer">
    <img src={imageIconSettings} alt="Icon" />
    <p>{textIconSettings}</p>
</div>

<style>
    .iconsContainer {
        display: flex;
        align-items: center;
        margin-bottom: 40px;
        cursor: pointer;
    }
    .iconsContainer:last-child {
        margin-bottom: 0;
    }
    .iconsContainer img {
        margin-right: 16px;
    }
</style>
