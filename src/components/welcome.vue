<template>
    <main>
        <div class="title">Получите бесплатный курс Английского со скидкой 100%</div>
        <div class="sub-title">Акция действует до 02/11/2021 24:00 <br> Спешите!!!</div>
        <img src="https://images.unsplash.com/photo-1455540904194-fc101941273a?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8ZW5nbGlzaHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="">
    </main>
</template>

<style scoped>
main{
    margin: 30px 0 20px 0;
}
.title{
    font-weight: 600;
    font-size: 56px;
    line-height: 130%;
    /* or 73px */
    letter-spacing: -0.01em;
    color: rgba(255, 255, 255, 0.8);
    text-align: center;
}
img{
    width: 100%;
    height: 50%;
    border-radius: 50%;
    margin: 30px 0;
}
.sub-title{
    font-size: 18px;
    line-height: 150%;
    /* identical to box height, or 27px */
    color: rgba(255, 255, 255, 0.4);
    text-align: center;
}
@media (max-width:700px) {
    .title{
        font-size: 36px;
    }
}
</style>