<script>
    import Stories from "./components/dashboard/Stories.svelte";
    import { DashboardStories } from "./data";
</script>

<div class="dashboard">
    <div class="containerDashboard">
        <div class="stories">
            <div class="addStories">
                <img src="/freelance/images/profile.png" alt="Photos profile" />
                <img src="/freelance/images/Icon-add.png" alt="Icon Add" />
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
        <div class="analitysAndDistribution">
            <div class="analyticsContainer">
                <p class="analyticsPrincipalTitle">Analytics</p>
                <div class="analyticsAndOther">
                    <div class="dailyViews">
                        <div class="dailyViewsHeader">
                            <p>Daily Views</p>
                            <div class="dailyViewsYear">
                                <p>2021</p>
                            </div>
                        </div>
                        <div class="dailyViewStats">
                            <img src="/freelance/images/stats.svg" alt="" />
                        </div>
                    </div>
                    <div class="analyticsMusic">
                        <div class="musicHeader">
                            <img src="/freelance/images/1.jpg" alt="" />
                            <div class="pauseIcon">
                                <img src="/freelance/images/icons/stopIcon.png" alt="" />
                            </div>
                        </div>
                        <div class="musicbody">
                            <p class="musicbodyTitle">
                                Strange Clouds Formation
                            </p>
                            <p class="musicbodyArtist">By Mike Taylor</p>
                        </div>
                    </div>
                    <div class="scheduled">
                        <div class="scheduledImage">
                            <img src="/freelance/images/icons/calendar.png" alt="" />
                        </div>
                        <p>Scheduled</p>
                    </div>
                    <div class="addNew">
                        <div class="addNewImage">
                            <img src="/freelance/images/icons/add2.png" alt="" />
                        </div>
                        <p>Add New</p>
                    </div>
                </div>
            </div>
            <div class="distributionContainer">
                <p class="distributionContainer">Events Distribution</p>
                <div class="distributionContent">
                    <p class="distributionContentTitle">
                        Last 30 Days Performance
                    </p>
                    <div class="distributionRadio">
                        <img src="/freelance/images/radio.svg" alt="" />
                    </div>
                    <p class="EventsDISTRIBUTION">Events DISTRIBUTION</p>
                    <div class="actionsDistribution">
                        <div class="likesDistro">
                            <div>
                                <img src="/freelance/images/icons/heart.svg" alt="" />
                            </div>
                            <p>Likes</p>
                        </div>
                        <div class="viewsDistro">
                            <div>
                                <img src="/freelance/images/icons/Swap.svg" alt="" />
                            </div>
                            <p>Views</p>
                        </div>
                        <div class="peopleDistro">
                            <div>
                                <img
                                    src="/freelance/images/icons/profileAdd.svg"
                                    alt=""
                                />
                            </div>
                            <p>Follow</p>
                        </div>
                        <div class="chatDistro">
                            <div>
                                <img src="/freelance/images/icons/Chat.svg" alt="" />
                            </div>
                            <p>Shares</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="Statistics">
            <p class="StatisticsTitle">Statistics</p>
            <div class="targets">
                <div class="whiteTarget">
                    <div class="whiteTargetText">
                        <p>Weekly Target</p>
                        <p>25% achieved</p>
                    </div>
                    <div class="whiteTargetLine" />
                    <div class="whiteTargetPorcent">25%</div>
                </div>
                <div class="otherTarget">
                    <div class="otherTargetText">
                        <p>Monthly Target</p>
                        <p>50% achieved</p>
                    </div>
                    <div class="otherTargetLine" />
                    <div class="otherTargetPorcent">50%</div>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .dashboard {
        grid-area: dashboard;
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
    .performance {
        margin-bottom: 70px;
    }
    .performaceTitle {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 35px;
    }
    .performancePost {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
        gap: 20px;
    }
    .performancePost div {
        max-width: 210px;
        width: 100%;
        min-height: 75px;
        padding: 16px 19px;
    }
    .views p:first-child,
    .follows p:first-child,
    .likes p:first-child {
        font-size: 14px;
        font-weight: bold;
        color: #9590d5;
        margin-bottom: 7px;
    }
    .views p:last-child,
    .follows p:last-child,
    .likes p:last-child {
        font-size: 14px;
        color: white;
    }
    .views {
        background: url("/freelance/images/views.png") no-repeat center / 100%;
    }
    .follows {
        background: url("/freelance/images/follows.png") no-repeat center/ 100%;
    }
    .likes {
        background: url("/freelance/images/likes.png") no-repeat center/ 100%;
    }
    .analitysAndDistribution {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-areas: "analytics" "distribution";
        gap: 31px;
        margin-bottom: 70px;
    }
    .analyticsAndOther {
        grid-area: analytics;
        display: grid;
        grid-template-columns: 1fr;
        grid-template-areas:
            "dailyNews"
            "music"
            "scheduled"
            "addNew";
        gap: 10px;
    }
    .dailyViews {
        grid-area: dailyNews;
    }
    .distributionContainer {
        grid-area: distribution;
    }
    .analyticsPrincipalTitle,
    .distributionContainer {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 20px;
    }
    .dailyViews {
        background-color: white;
        border-radius: 10px;
        padding: 10px 19px;
        margin-bottom: 33px;
    }
    .dailyViewsHeader {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 26px;
    }
    .dailyViewsHeader > p {
        font-size: 12px;
        font-weight: bold;
    }
    .dailyViewsHeader .dailyViewsYear p {
        font-size: 8.84px;
    }
    .dailyViewStats img {
        width: 100%;
        object-fit: cover;
    }
    .analyticsMusic {
        width: 100%;
        background-color: #f2e9ff;
        border-radius: 10px;
        padding: 19px;
    }
    .analyticsMusic .musicHeader {
        display: flex;
        justify-content: space-between;
        margin-bottom: 14px;
    }
    .analyticsMusic .musicHeader > img {
        width: 67px;
        height: 67px;
        object-fit: cover;
        border-radius: 10px;
    }
    .analyticsMusic .musicHeader .pauseIcon {
        background-color: #51459e;
        width: 35px;
        height: 43px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 27px;
        cursor: pointer;
    }
    .musicbodyTitle {
        font-size: 13px;
        font-weight: bold;
        margin-bottom: 5px;
    }
    .musicbodyArtist {
        font-size: 10px;
        color: #7b7b7b;
    }
    .scheduled,
    .addNew {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        border-radius: 10px;
        background-color: white;
        text-align: center;
    }
    .scheduledImage,
    .addNewImage {
        background-color: #84e8f4;
        width: 35px;
        height: 43px;
        border-radius: 27px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .distributionContainer {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 32px;
        height: max-content;
    }
    .distributionContent {
        background-color: white;
        border-radius: 10px;
        padding: 20px 18px;
    }
    .distributionContentTitle {
        font-size: 12px;
        font-weight: bold;
        text-align: center;
        margin-bottom: 30px;
    }
    .distributionRadio {
        display: flex;
        justify-content: center;
        margin-bottom: 23px;
    }
    .EventsDISTRIBUTION {
        font-size: 10.97px;
        font-weight: bold;
        text-align: center;
        margin-bottom: 23px;
    }
    .actionsDistribution {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 5px;
    }
    .likesDistro,
    .viewsDistro,
    .peopleDistro,
    .chatDistro {
        display: flex;
        align-items: center;
        margin-bottom: 15px;
    }
    .likesDistro div,
    .viewsDistro div,
    .peopleDistro div,
    .chatDistro div {
        width: 25.06px;
        height: 25.06px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-right: 5px;
        cursor: pointer;
    }
    .likesDistro div {
        background-color: #f8896b;
    }
    .viewsDistro div {
        background-color: #84e7f3;
    }
    .peopleDistro div {
        background-color: #ffbc65;
    }
    .chatDistro div {
        background-color: #51459e;
    }
    .likesDistro p,
    .viewsDistro p,
    .peopleDistro p,
    .chatDistro p {
        font-size: 10px;
        font-weight: 400;
    }
    .StatisticsTitle {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 20px;
    }
    .targets {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
        gap: 10px;
        margin-bottom: 20px;
    }
    .whiteTarget,
    .otherTarget {
        width: 100%;
        border-radius: 10px;
        padding: 17px 32px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .whiteTarget {
        background-color: white;
    }
    .otherTarget {
        background-color: #51459e;
        color: white;
    }
    .whiteTargetLine {
        background-color: #f6f6fc;
    }
    .otherTargetLine {
        background-color: #ffffff;
    }
    .whiteTargetLine,
    .otherTargetLine {
        height: 100%;
        width: 1px;
    }
    .whiteTargetText p:first-child,
    .otherTargetText p:first-child {
        font-weight: bold;
        font-size: 18px;
        margin-bottom: 9px;
    }
    .whiteTargetText p:last-child,
    .otherTargetText p:last-child {
        font-size: 13px;
    }
    .whiteTargetPorcent {
        color: #4d4a81;
    }
    .otherTargetPorcent,
    .whiteTargetPorcent {
        width: 75px;
        height: 75px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        border: 5px solid #f9896b;
        font-size: 17px;
        font-weight: bold;
    }
    @media (min-width: 768px) {
        .analitysAndDistribution {
            grid-template-columns: 2fr 1fr;
            grid-template-areas: "analytics distribution";
        }
        .analyticsAndOther {
            grid-area: analytics;
            grid-template-columns: 2fr 1fr 1fr;
            grid-template-areas:
                "dailyNews dailyNews dailyNews"
                "music scheduled addNew";
            gap: 10px;
        }
    }
</style>
