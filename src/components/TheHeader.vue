<script setup>
import SearchInput from '@/shared/components/SearchInput.vue'
import IconSearch from '@/shared/components/icons/IconSearch.vue'
import TheMainLogo from '@/components/TheMainLogo.vue'
import IconWhatsApp from '@/shared/components/icons/IconWhatsApp.vue'
import IconTg from '@/shared/components/icons/IconTg.vue'
import IconViber from '@/shared/components/icons/IconViber.vue'
import TheButton from '@/components/buttons/TheButton.vue'
</script>

<template>

    <div class="header">
        <div class="logo_time">
            <RouterLink to="/">
                <TheMainLogo class="logo" />
            </RouterLink>
            <p>Ежедневно с 9:00 до 21:00</p>
        </div>

        <div class="header-container">
            <div class="search-container">
                <SearchInput class="search-input" />
                <div class="search-overlay">
                    <IconSearch />
                    <span class="search-label">Поиск по сайту</span>
                </div>
            </div>


        </div>

        <div class="calc">
            <RouterLink to="/">
                <p class="calc_word">Калькулятор</p>
            </RouterLink>
        </div>

        <div class="social">

            <IconWhatsApp />


            <IconTg class="ico" />


            <IconViber />

        </div>
        <div class="phone_email">
            <p class="phone_email-phone">+7 (812) 926-88-33</p>
            <p class="phone_email-mail">info@eco-lom.ru</p>
        </div>

        <div class="call-me">
            <TheButton class="call-me_btn">Перезвоните мне</TheButton>
        </div>
    </div>
    <div class="nav">
        <RouterLink to="/">
            <p class="nav_item">ЛОТЕРЕЯ</p>
        </RouterLink>
        <RouterLink to="/">
            <p class="nav_item">МЕТАЛЛОЛОМ</p>
        </RouterLink>
        <RouterLink to="/">
            <p class="nav_item">УСЛУГИ</p>
        </RouterLink>
        <RouterLink to="/">
            <p class="nav_item">ЦЕНЫ</p>
        </RouterLink>
        <RouterLink to="/">
            <p class="nav_item">ПУНКТЫ ПРИЕМА</p>
        </RouterLink>
        <RouterLink to="/">
            <p class="nav_item">О КОМПАНИИ</p>
        </RouterLink>
        <RouterLink to="/">
            <p class="nav_item">КОНТАКТЫ</p>
        </RouterLink>
    </div>

</template>


<style lang="scss" scoped>
@import '@/style/modules/mixins.scss';

.header {
    width: 100%;
    height: 11.1rem;
    border-bottom: 1px solid #e8e8e8;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding-left: 31.2rem;
    padding-right: 31.2rem;
}

.logo {
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: start;
}

.calc_word {
    cursor: pointer;
    color: #105720;
    font-size: 1.6rem;
    text-decoration: underline;
}

.phone_email {
    display: flex;
    flex-direction: column;
}

.phone_email-phone {
    @include font-setup('OpenSans-Regular', 1.6rem, 600);
    font-size: 1.6rem;
}

.phone_email-mail {
    @include font-setup('OpenSans-Regular', 1.6rem, 400);
    font-size: 1.6rem;
    color: #1F1F1F;
}

.header-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 20px 0 20px;
}

.search-container {
    position: relative;
    width: 215px;
    height: 46px;
}

.search-input {
    width: 100%;
    height: 100%;
    padding: 0 20px;
    background-color: #FFF7F3;
    border: none;
    border-radius: 100px;
    color: transparent;
    outline: none;
}

.search-label {
    padding-left: 1rem;
    color: #F95707;
}

.search-overlay {
    position: absolute;
    top: 20%;
    left: 15%;
    display: flex;
    justify-content: space-between;

    align-items: center;
    font-size: 1.6rem;
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


.social {
    display: flex;
    flex-direction: row;
    padding: 0 1.2rem 0 1.2rem;
    cursor: pointer;
}

.ico {
    margin: 0 1.2rem 0 1.2rem;
}



.nav {
    border-bottom: 1px solid #e8e8e8;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 6.7rem;
    padding-left: 31.2rem;
    padding-right: 31.2rem;

    .nav_item {
        cursor: pointer;
        position: relative;
    }

    .nav_item::after {
        display: block;
        position: absolute;
        left: 0;
        width: 0;
        height: 2px;
        background-color: #F95707;
        content: "";
    }

    .nav_item:hover:after,
    .nav_item:focus:after {
        width: 100%;
    }
}
</style>