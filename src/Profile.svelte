<div class="profile">
    <div class="greating">
        <div class="greatingText">
            <p>Hi Shakir</p>
            <p>Good Morning!</p>
        </div>
        <div class="greatingIcons">
            <div>
                <img src="/images/icons/chat.png" alt="Chat Icon" />
            </div>
            <div>
                <img src="/images/icons/notify.png" alt="Notify Icon" />
            </div>
        </div>
    </div>
    <div class="profileContent">
        <img src="/images/profile.png" alt="Photos Profile" />
        <div class="profileName">
            <p>AR Shakir</p>
            <p>UI/UX Designer @Redwhale</p>
        </div>
        <div class="profileStats">
            <div class="followers">
                <p>786K</p>
                <p>Followers</p>
            </div>
            <div class="following">
                <p>298</p>
                <p>Following</p>
            </div>
            <div class="post">
                <p>438</p>
                <p>Post</p>
            </div>
        </div>
    </div>
    <div class="profileButtonActions">
        <div class="view">
            <p>View Profile</p>
        </div>
        <div class="edit">
            <p>Edit Profile</p>
        </div>
    </div>
    <div class="profileMultimedia">
        <div class="video">
            <div class="xIcon">x</div>
            <img class="image" src="/images/icons/video.png" alt="Video" />
            <div>
                <p>Videos</p>
                <p>Click To Add Video.</p>
            </div>
        </div>
        <div class="photo">
            <div class="xIcon">x</div>
            <img class="image" src="/images/icons/camera.png" alt="Photos" />
            <div>
                <p>Photos</p>
                <p>Click To Add Photo.</p>
            </div>
        </div>
    </div>
    <div class="imagesGrid">
        <img src="/images/1.jpg" alt="">
        <img src="/images/2.jpg" alt="">
        <img src="/images/3.jpg" alt="">
        <img src="/images/4.jpg" alt="">
        <img src="/images/5.jpg" alt="">
        <img src="/images/6.jpg" alt="">
    </div>
</div>

<style>
    .profile {
        background-color: white;
        min-height: 100vh;
        padding: 47px 20px;
        overflow-y: auto;
        overflow-x: hidden;
    }
    .profile::-webkit-scrollbar {
        width: 10px;
    }
    .profile::-webkit-scrollbar-track {
        background: orange;
    }

    .profile::-webkit-scrollbar-thumb {
        background-color: #fafafa;
        border-radius: 20px;
        border: 3px solid orange;
    }
    .greating {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 78px;
    }
    .greatingText p:first-child {
        font-size: 18px;
        font-weight: bold;
    }
    .greatingText p:last-child {
        font-size: 14px;
        color: #707a89;
    }
    .greatingIcons {
        display: flex;
        align-items: center;
    }
    .greatingIcons div {
        width: 48px;
        height: 48px;
        border: 1px solid #efeeee;
        border-radius: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-left: 10px;
        cursor: pointer;
    }
    .profileContent {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .profileContent img {
        box-shadow: 1px 1px 75px 60px #f7ede4;
        margin-bottom: 30px;
    }
    .profileName p {
        text-align: center;
    }
    .profileName p:first-child {
        font-size: 18px;
        font-weight: bold;
        margin-bottom: 7px;
    }
    .profileName p:last-child {
        font-size: 12px;
        color: #707a89;
        margin-bottom: 26px;
    }
    .profileStats {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        margin-bottom: 24px;
    }
    .followers,
    .following,
    .post {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .followers p:first-child,
    .following p:first-child,
    .post p:first-child {
        font-weight: bold;
        font-size: 16px;
    }
    .followers p:last-child,
    .following p:last-child,
    .post p:last-child {
        font-size: 12px;
    }
    .profileButtonActions {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        margin-bottom: 35px;
    }
    .profileButtonActions > div {
        border-radius: 10px;
        height: 40px;
        width: 48%;
    }
    .profileButtonActions .view {
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: #4f46ba;
        color: white;
        cursor: pointer;
    }
    .profileButtonActions .edit {
        display: flex;
        justify-content: center;
        align-items: center;
        border: 1px solid #e6e6eb;
    }
    .profileMultimedia{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 37px;
    }
    .profileMultimedia > div {
        min-height: 193px;
        border-radius: 10px;
        width: 48%;
    }
    .profileMultimedia .video, .profileMultimedia .photo{
        padding: 17px;
    }
    .profileMultimedia .video{
        background-color: #f2e9ff;
    }
    .profileMultimedia .photo{
        background-color: #fef3f0;
    }
    .xIcon{
        width: 100%;
        font-weight: bold;
        display: flex;
        justify-content: flex-end;
        cursor: pointer;
        margin-bottom: 30px;
    }
    .profileMultimedia .video .image, .profileMultimedia .photo .image{
        width: 45px;
        height: 45px;
        object-fit: contain;
        margin-bottom: 19px;
    }
    .photo div p:first-child, .video div p:first-child{
        font-weight: bold;
        font-size: 22px;
    }
    .photo div p:last-child, .video div p:last-child{
        font-weight: bold;
        font-size: 12px;
    }
    .video div p:first-child, .video div p:last-child{
        color: #51459e;
    }
    .photo div p:first-child, .photo div p:last-child{
        color: #ac6755;
    }
    .imagesGrid{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
        gap: 5px;
    }
    .imagesGrid img{
        min-width: 80px;
        width: 100%;
        height: 111px;
        object-fit: cover;
    }
</style>
