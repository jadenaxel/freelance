<script>
    export let StoriePeopleImage, StoriePeopleName, StorieHas;
</script>

<div class="stories">
    <img
        src={StoriePeopleImage}
        alt="Photos profile"
        class={StorieHas ? "storiesHas" : ""}
    />
    <p>{StoriePeopleName}</p>
</div>

<style>
    .stories {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        margin-right: 14px;
    }
    .stories:last-child{
        margin-right: 0;
    }
    img {
        width: 53px;
        height: 53px;
        border-radius: 50%;
        margin-bottom: 8px;
    }
    .storiesHas {
        border: 1px solid #ff9a9a;
    }
    p {
        font-size: 10px;
        text-align: center;
    }
</style>
