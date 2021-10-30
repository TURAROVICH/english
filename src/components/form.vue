<template>
 <form @submit.prevent="send" class="form" id="form">
     <div v-if="error" class="error">{{error}}</div>
    <input minlength="5" type="text" v-model="name" placeholder="Имя" required>
    <input type="email" v-model="email" placeholder="Email" required>
    <input type="password" minlength="8" v-model="password" placeholder="Пароль" required>
    <!-- your other form fields go here -->
    <button  type="submit"><span>Получить курс!</span></button>
</form>
</template>

<script>
import axios from 'axios'
export default {
    data:()=>({
        name:'',
        email:'',
        password:'',
        error:''
    }),
    methods:{
        send(){
            // if(!this.name.trim()){
            //     return this.error = 'Поле имя заполнен не корректно!'
            // }
            // if(!this.email.trim()){
            //     return this.error = 'Поле email заполнен не корректно!'
            // }
            // if(!this.password.trim()){
            //     return this.error = 'Поле password заполнен не корректно!'
            // }
            let data = {
                name:this.name,
                email:this.email,
                password:this.password
            }
            axios.post('https://formspree.io/f/xdoyrovj',data)
                .then(()=>this.error='В течении 5-минут мы отправим вам ссылку!)')
                .catch(()=>this.error="Ошибка! Отправте форму еще раз пожалуйста(")
        }
    }

}
</script>

<style scoped>
.error{
    font-size: 32px;
    color: #fff;
}
.form{
    display: flex;
    flex-direction: column;
    margin: 20px 0 60px 0;
    gap :15px;

}
input{
    background: #1F2143;
    border-radius: 12px;
    height: 42px;
    outline: none;
    border:none;
    padding: 0 30px;;
    color:#fff;
}
button{
    background: #F5443B;
    border-radius: 6px;
    height: 50px;
    border:none;
    outline:none;
}
button span{
    font-size: 14px;
    line-height: 17px;
    /* identical to box height */
    color: #FFFFFF;
}
</style>

