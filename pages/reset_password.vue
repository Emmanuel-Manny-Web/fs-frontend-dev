<script>
import { useAuthStore } from '~~/store/auth'

export default {
    data() {
        return {
            password1: "",
            password2: "",
        }
    },
    methods: {
        async resetPassword() {
            const email = useAuthStore().$state.user.email
            const config = useRuntimeConfig()
            const res = await useFetch(
                `${config.public.baseURL}/users/reset-password/`,
                {
                    'method': 'post',
                    'body': {
                        email: email,
                        password: this.password1
                    }
                }
            )
            if (res.data.value) {
                this.$router.push('/reset_password_successful')
            } else {
                useNotification().toast.error(res.error.value.data.message)
            }
        }
    }
}
</script>

<template>
    <main>
        <section class="sectioni">
            <img src="~/assets/logo.png" alt="" class="logo" />
            <p class="t1">Reset Password</p>
            <p class="t2">Fill in your details to continue</p>
            <form @submit.prevent="resetPassword">
                <span class="spf">
                    <label htmlFor="password">Enter new password</label>
                    <span class='inp'><input v-model.trim="password1" type="password" name="" id="" placeholder='Password' required />
                        <Icon name="bi:eye" />
                    </span>
                </span>

                <span class="spf">
                    <label htmlFor="password">Confirm new password</label>
                    <span class='inp'><input v-model.trim="password2" type="password" name="" id="" placeholder='Password' required /></span>
                </span>

                <button type="submit">
                    Reset password
                </button>
            </form>
        </section>
        <section class="section2">
            <div>
                <p class='q'><em>"</em></p>
                <p class='quote'>Creating seamless exchange procedure for everyone. Buy, sell, save, trade and exchange
                    fiat currencies with 3 simple steps. </p>
                <p class="author">Abisola Omotayo</p>
                <p class="role">Founder, GirlsInTech</p>
            </div>
        </section>
    </main>
</template>

<style scoped>
main {
    width: 100%;
    height: 100vh;
    background-color: white;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 20px 20px;
    padding-left: 0;
}


main section {
    /* width: 50%; */
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /* border: solid; */
}

main .sectioni {
    width: 55% !important;
    row-gap: 10px;
}

main .sectioni .logo {
    margin-bottom: 10px;
}

main .sectioni .t1 {
    font-family: 'lora', sans-serif;
    font-size: 22px;
    font-weight: 700;
    text-align: center;
    /* width: 10%; */
}

main .sectioni .t2 {
    font-size: 14px;
    text-align: center;
}

main .sectioni .email_img {
    margin: 10px 0;
    margin-top: -10px;
}

main .sectioni .et1 {
    font-family: 'lora', sans-serif;
    font-size: 26px;
    font-weight: 700;
    text-align: center;
    margin-bottom: 10px;
}

main .sectioni .et2 {
    font-size: 16px;
    width: 50%;
    text-align: center;
}

main .sectioni .ea {
    margin: 5% 0;
}

main .sectioni .ea a {
    color: #2F67FA;
    margin-left: 10px;
}

main .sectioni .gbck {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    color: #2F67FA;
    border: solid 1px;
    border-radius: 30px;
    padding: 12px 30px;
}

main .sectioni form {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    width: 360px;
    margin-top: 20px;
    row-gap: 30px;
}

main .sectioni form p {
    text-align: center;
}

main .sectioni form .spf {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    width: 100%;
    margin: 0;
    row-gap: 10px;
}

main .sectioni form label {
    font-size: 14px;
    text-transform: capitalize;
    font-weight: 500;
    letter-spacing: 0.4px;
}

main .sectioni form input {
    width: 100%;
    height: 45px;
    border-radius: 30px;
    padding: 0 25px;
    border: none;
    outline: none 1px silver;
    /* margin: 10px 0 0 0; */
    background: #FFFFFF;
    border: 1px solid #DCDEE5;
    border-radius: 48px;
}

main .sectioni form input::placeholder {
    font-size: 15px;
    letter-spacing: .5px;
    font-weight: 300;
    color: #7C859D;
}

main .sectioni form .inp {
    width: 100%;
    height: 45px;
    border-radius: 30px;
    padding: 0 25px;
    border: none;
    outline: none 1px silver;
    /* margin: 10px 0 14px 0; */
    background: #FFFFFF;
    border: 1px solid #DCDEE5;
    border-radius: 48px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    overflow: hidden;
}

main .sectioni form .inp input {
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    margin: 0;
    padding: 0;
    border-radius: 0;
    /* border: solid; */
}

main .sectioni form .inp i {
    height: 100%;
    padding: 0 0;
    font-size: 26px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #7C859D;
    font-weight: 100;
    cursor: pointer;
}

main .sectioni form .forgot {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    color: #2F67FA;
    text-decoration: none;
    text-align: right;
    font-size: 14px;
    /* margin-top: -6px;
    margin-bottom: 18px; */
}

main .sectioni form button {
    width: 100%;
    height: 50px;
    border-radius: 48px;
    color: white;
    font-size: 17px;
    background-color: #2F67FA;
    border: none;
    /* margin-bottom: 20px; */
    font-weight: 500;
}

main .sectioni form .tc {
    width: 100%;
    font-size: 14px;
    color: #7C859D;
    font-weight: 400;
    width: 280px;
    margin: 0 auto;
    line-height: 150%;
}

main .sectioni form .tc a {
    color: #18191B;
    text-decoration: none;
    font-weight: 500;
}

main .sectioni form .or {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    /* margin: 20px 0; */
}

main .sectioni form .or span {
    width: 100%;
    height: 0.01px;
    border-bottom: solid 0.03px #7C859D;
}

main .sectioni form .or p {
    text-transform: uppercase;
    margin: 0 10px;
    font-size: 14px;
}

main .sectioni form .social_in {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    row-gap: 10px;
}

main .sectioni form .social_in a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 45px;
    border: solid 1px #DCDEE5;
    border-radius: 48px;
    text-decoration: none;
    color: #8f9094;
    gap: 10px;
}

main .sectioni form .already {
    text-align: center;
    display: flex;
    align-items: center;
    font-size: 16px;
    color: #7C859D;
    gap: 10px;
    width: 100%;
    justify-content: center;
    /* margin-top: 15px; */
    color: #18191B;
}

main .sectioni form .already a {
    color: #2F67FA;
}

main .sectioni form .pass {
    width: 100%;
    height: fit-content;
    display: flex;
    justify-content: space-between;
    align-items: center;
    /* border: solid; */
}

main .sectioni form .pass .sp {
    width: 50%;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-direction: column;
    row-gap: 15px;
    /* border: solid; */
}

main .sectioni form .pass .sp h3 {
    font-weight: 400;
    font-size: 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row;
    text-align: left;
}

main .sectioni form .pass .sp h3 div {
    width: 10px;
    height: 10px;
    border-radius: 100%;
    background-color: #D9D9D9;
    /* background-color: #148F18; */
    margin-right: 8px;
}

main .sectioni form .pass .sp h3 .bll {
    background-color: #148F18;
}

main .sectioni form .pass .sp h3 .ggg {
    background-color: #D9D9D9;
}


main .sectioni .to {
    text-align: center;
    font-size: 18px;
    line-height: 150%;
    margin-top: 30px;
}

main .sectioni .to .ap {
    font-weight: 700;
}

main .sectioni .form2 {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    width: fit-content;
    margin-top: 25px;
    row-gap: 0px;
}

main .sectioni .to2 .ap {
    margin-left: 5px;
}

main .sectioni .form2 .ct {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 15px;
}

main .sectioni .form2 .ct input {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 60px;
    height: 60px;
    border-radius: 10px;
    padding: 0;
    margin: 0;
    font-size: 30px;
    /* padding: 20px 20px; */
    padding-left: 23px;
}

main .sectioni .to2 .a {
    color: #2F67FA;
    font-weight: 600;
    margin-left: 3px;
}

main .sectioni .form2 button {
    margin-top: 35px;
    font-size: 20px;
    cursor: pointer;
    height: 55px;
    font-weight: 500;
}

main .sectioni .form2 .already {
    margin-top: 40px;
}

main .section2 {
    width: 45% !important;
    background-image: url(./assets/girl_img.svg);
    justify-content: flex-end;
    padding: 20px 20px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
    border-top-left-radius: 80px;
    border-bottom-right-radius: 80px;
    /* border: solid; */
}

main .bg2 {
    background-image: url(./images/boy_bck.svg);
}

main .section2 div {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    background: linear-gradient(98.29deg, rgba(255, 255, 255, 0.4) -3.61%, rgba(255, 255, 255, 0.2) 103.7%);
    backdrop-filter: blur(10.5px);
    border-radius: 16px 16px 80px 16px;
    padding: 20px 30px;
}

main .section2 div .quote {
    color: #FFFFFF;
    font-size: 19px;
    font-weight: 500;
    width: 80%;
    margin-bottom: 8%;
}

main .section2 div .q {
    font-size: 30px;
    color: white;
    line-height: 20px;
    width: 10px;
}

main .section2 div .author {
    color: #FFFFFF;
    font-size: 18px;
    font-weight: 500;
    font-family: 'lora', sans-serif;
}

main .section2 div .role {
    color: #FFFFFF;
    font-size: 18px;
    font-weight: 400;
    font-size: 14px;
    line-height: 150%;
    margin-top: 2px;
}









@media screen and (max-width: 950px) {
    main {
        width: 100%;
        height: fit-content;
        background-color: white;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        padding: 20px 10px;
        padding-left: 10px;
        /* border: solid; */
    }

    main .sectioni {
        width: 100% !important;
        padding: 30px 0;
        padding-bottom: 50px;
    }

    main .sectioni .t1 {
        width: 70%;
        /* border: solid; */
    }

    main .sectioni form {
        width: 90%;
        margin-top: 50px;
        row-gap: 25px;
        max-width: 400px;
    }

    main .sectioni form input {
        width: 100%;
        height: 50px;
        border-radius: 30px;
    }

    main .sectioni form .inp {
        width: 100%;
        height: 50px;
        border-radius: 30px;
    }

    main .sectioni .to {
        font-size: 16px;
        margin-top: 30px;
        width: 75%;
        /* border: solid; */
    }


    main .section2 {
        width: 100% !important;
        border-top-left-radius: 80px;
        border-bottom-right-radius: 80px;
        height: 600px;
    }

    main .section2 div .quote {
        width: 100%;
        margin-bottom: 8%;
    }

    main .sectioni .et2 {
        width: 70%;
    }

    main .sectioni .form2 .ct {
        gap: 12px;
    }


    main .sectioni .form2 .ct input {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        border-radius: 10px;
        font-size: 20px;
        padding-left: 16px;
    }

    main .sectioni .form2 button {
        margin-top: 35px;
        font-size: 18px;
        cursor: pointer;
        height: 55px;
        font-weight: 500;
    }


}






@media screen and (max-width: 700px) {
    main .sectioni {
        padding: 10px 0;
        padding-bottom: 50px;
    }

    main .sectioni .t1 {
        font-size: 20px;
        line-height: 150%;
        width: 180px;
        /* border: solid; */
    }

    main .sectioni .t2 {
        font-size: 14px;
        margin-top: 0px;
    }

    main .sectioni form {
        row-gap: 30px;
        margin-top: 30px;
    }

    main .sectioni form .spf {
        row-gap: 15px;
    }

    main .sectioni form label {
        font-size: 15px;
        letter-spacing: 0px;
    }

    main .sectioni form input {
        width: 100%;
        height: 45px;
        border-radius: 30px;
        padding: 0 20px;
        border: 1.5px solid #DCDEE5;
        border-radius: 10px;
    }

    main .sectioni form input::placeholder {
        font-size: 15px;
        letter-spacing: 0px;
        font-weight: 400;
        color: #7C859D;
    }

    main .sectioni form .inp {
        width: 100%;
        height: 45px;
        border-radius: 30px;
        padding: 0 20px;
        border: none;
        outline: none 1px silver;
        /* margin: 10px 0 14px 0; */
        background: #FFFFFF;
        border: 1.5px solid #DCDEE5;
        border-radius: 10px;
    }


    /* main{
       display: flex; flex-direction: column; justify-content: space-between; align-items: center;
       border: solid black !important;
    } */

}</style>