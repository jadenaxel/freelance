<script>
    import Stories from "./components/dashboard/Stories.svelte";
    import { DashboardStories } from "./data";
</script>

<div class="dashboard">
    <div class="containerDashboard">
        <div class="stories">
            <div class="addStories">
                <img src="/images/profile.png" alt="Photos profile" />
                <img src="/images/Icon-add.png" alt="Icon Add" />
                <p>Add to</p>
            </div>
            {#each DashboardStories as item}
                <Stories
                    StoriePeopleImage={item.StoriePeopleImage}
                    StoriePeopleName={item.StoriePeopleName}
                    StorieHas={item.StorieHas}
                />
            {/each}
        </div>
        <div class="performance">
            <p class="performaceTitle">30 Days Performance</p>
            <div class="performancePost">
                <div class="views">
                    <p>Views</p>
                    <p>7,482,120</p>
                </div>
                <div class="follows">
                    <p>Follows</p>
                    <p>54,364</p>
                </div>
                <div class="likes">
                    <p>Likes</p>
                    <p>125,685</p>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .dashboard {
        padding-top: 39px;
    }
    .stories {
        display: flex;
        justify-content: space-between;
        width: 100%;
        overflow-x: scroll;
        margin-bottom: 62px;
    }
    .stories::-webkit-scrollbar {
        display: none;
    }
    .addStories {
        width: 55px;
        position: relative;
        cursor: pointer;
        margin-right: 14px;
    }
    .addStories img:first-child {
        width: 53px;
        height: 53px;
        border-radius: 50%;
    }
    .addStories img:last-of-type {
        width: 15px;
        height: 15px;
        position: absolute;
        right: 0;
        bottom: 10px;
        margin-bottom: 10px;
    }
    .addStories p {
        font-size: 10px;
        text-align: center;
    }
    .performaceTitle {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 35px;
    }
    .performancePost {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    }
    .performancePost div{
        max-width: 210px;
        width: 100%;
        height: 75px;
        padding: 16px 19px;
    }
    .views p:first-child, .follows p:first-child, .likes p:first-child{
        font-size: 14px;
        font-weight: bold;
        color: #9590d5;
        margin-bottom: 7px;
    }
    .views p:last-child, .follows p:last-child, .likes p:last-child{
        font-size: 14px;
        color: white;
    }
    .views {
        background: url("/images/views.png") no-repeat center / 100%;
    }
    .follows{
        background: url("/images/follows.png") no-repeat center/ 100%;
    }
    .likes{
        background: url("/images/likes.png") no-repeat center/ 100%;
    }
</style>
