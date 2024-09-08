<script setup>
import TheButton from '@/components/buttons/TheButton.vue'
import IconPlay from '@/shared/components/icons/IconPlay.vue'
</script>


<template>
    <div class="main">
        <div class="main-header_buttons">
            <div class="main_header">
                <h1 class="h1-main">Приём лома чёрных<br> и цветных металлов<br> <span class="h1_green">в
                        Санкт-Петербурге</span> </h1>
            </div>

            <div class="btn_group">
                <div class="btn_group-1">
                    <TheButton class="call-me_btn btn-2">Цены на сегодня</TheButton>
                    <TheButton class="call-me_btn">Как сдать металл</TheButton>
                </div>
                <div class="btn_group-2">
                    <TheButton class="call-me_btn btn-2">Отзывы</TheButton>
                    <TheButton class="call-me_btn">Акции</TheButton>

                </div>
                <TheButton class="btn-reverse">Оставить заявку</TheButton>
            </div>
        </div>

        <div class="play">
            <svg width="200" height="200" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <!-- Определение пути для текста -->
                <defs>
                    <path id="textCircle" d="M 100, 100 m -75, 0 a 75,75 0 1,1 150,0 a 75,75 0 1,1 -150,0" />
                </defs>

                <!-- Иконка SVG -->
                <g transform="translate(90, 85)">
                    <IconPlay class="play_icon" />
                </g>

                <!-- Текст по кругу -->
                <text font-size="14" fill="#105720">
                    <textPath href="#textCircle" startOffset="50%" text-anchor="middle">
                        Видео о компании «ЭКОЛОМ» Видео о компании «ЭКОЛОМ»
                    </textPath>
                </text>
            </svg>
        </div>

        <div class="main_picture">
            <img alt="main_pic" src="@/assets/img/picture_main.png">
        </div>
    </div>
</template>


<style lang="scss">
@import '@/style/modules/mixins.scss';

.main {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    width: 100%;
    height: 68.9rem;
    background-color: #F3F7F4;
}

.main-header_buttons {
    display: flex;
    flex-direction: column;
}

.h1-main {
    @include font-setup('OpenSans-SemiBold', 4.8rem, 600);
    font-size: 4.8rem;
    color: #1F1F1F;
}

.h1_green {
    color: #105720;
}

.call-me_btn {
    cursor: pointer;
    color: #F95707;
    background-color: white;
    border: 1px solid #F95707;
    border-radius: 100px;
    padding: 12px 32px;
    font-size: 1.6rem;

    &:hover {
        color: white;
        background-color: #F95707;
        transition: 0.7s;
    }
}

.btn-2 {
    margin-right: 1.2rem;
}

.btn_group-1 {
    margin-bottom: 1.2rem;

}

.btn-reverse {
    cursor: pointer;
    color: white;
    background-color: #F95707;
    border: 1px solid #F95707;
    border-radius: 100px;
    padding: 12px 32px;
    font-size: 1.6rem;

    margin-top: 7.2rem;

    &:hover {
        color: #F95707;
        background-color: white;
        transition: 0.7s;
    }
}

.play_icon {
    cursor: pointer;
}
</style>