<script>
    import SettingOptions from "./components/settings/SettingsOptions.svelte";
    import SettingPost from "./components/settings/SettingsPost.svelte";
    import { settingsOptionsValues, settingPostValue } from "./data";
</script>

<div class="settings">
    <div>
        <div class="logo">
            <img src="/images/logo.png" alt="Logo" />
            <div class="logotipo">
                <h1>Redwhale</h1>
                <p>Growth & Marketing</p>
            </div>
        </div>
        {#each settingsOptionsValues as item}
            <SettingOptions
                imageIconSettings={item.imageIconSettings}
                textIconSettings={item.textIconSettings}
            />
        {/each}
        <div class="detailsContainer">
            <details>
                <summary>Posts</summary>
                {#each settingPostValue as item}
                    <SettingPost
                        settingPostIcon={item.settingPostIcon}
                        settingPostTitle={item.settingPostTitle}
                        settingPostQuantity={item.settingPostQuantity}
                    />
                {/each}
            </details>
            <img
                class="postAddIcon"
                src="/images/icons/add.png"
                alt="Add icon"
            />
        </div>
        <div class="favoriteContainer">
            <details>
                <summary>Favorite Users</summary>
            </details>
            <img
                class="postAddIcon"
                src="/images/icons/add.png"
                alt="Add icon"
            />
        </div>
    </div>
    <footer>
        <img src="/images/icons/add.png" alt="Add icon" />
        <p>Invite new member</p>
    </footer>
</div>

<style>
    .settings {
        background-color: white;
        min-height: 100vh;
        padding: 47px 35px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        overflow-y: auto;
        overflow-x: hidden;
        display: none;
    }
    .settings::-webkit-scrollbar {
        width: 10px;
    }
    .settings::-webkit-scrollbar-track {
        background: orange;
    }

    .settings::-webkit-scrollbar-thumb {
        background-color: #fafafa;
        border-radius: 20px;
        border: 3px solid orange;
    }
    .logo {
        display: flex;
        align-items: center;
        margin-bottom: 83px;
    }
    .logo img {
        margin-right: 9px;
    }
    .logotipo h1 {
        font-size: 17px;
        font-weight: bold;
        color: #6d6d6d;
    }
    .logotipo p {
        color: #a6a6a6;
        font-size: 12px;
        font-weight: bold;
    }
    .detailsContainer {
        margin-bottom: 50px;
    }
    .detailsContainer,
    .favoriteContainer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-top: 1px solid #e2e2e2;
        padding-top: 15px;
    }
    .favoriteContainer {
        margin-bottom: 20px;
    }
    .postAddIcon {
        align-self: flex-start;
        margin-top: 19px;
    }
    .detailsContainer details summary,
    .favoriteContainer details summary {
        padding: 1rem 0 37px;
        position: relative;
        cursor: pointer;
    }
    footer {
        display: flex;
        align-items: center;
    }
    footer img {
        margin-right: 15px;
    }
    @media (min-width: 1280px) {
        .settings {
            display: block;
        }
    }
</style>
