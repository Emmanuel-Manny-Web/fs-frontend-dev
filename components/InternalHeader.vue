<template>
    <header class="blog_head">
        <nav class="nav-fixed">
            <Notification_bar />
            <Sidenav />
            <NuxtLink to='/' class='logo_a'> <img src="~/assets/logo.png" alt="wame" class='logo' /></NuxtLink>
            <div class='sp'>
                <a to='/blog_index' class='a'>Our blog</a>
                <a to='/contactus' class='a'>Contact us</a>
                <a to="/seller_up" class='a'>Become a seller</a>
                <a to='' class='a'>P2P marketplace</a>
            </div>
            <div class="user">
                <div class="n_icon">
                    <i class="material-icons-outlined bell">notifications</i>
                    <div class="not"></div>
                </div>

                <div class="profile">
                    <div class='prof'>
                        <div class="user_descrpt">
                            <p class="username">Maverick Egubson</p>
                            <p class="usermail">maverick.eth@gmail.com</p>
                        </div>
                        <div class="userimage">
                            <p class="me">ME</p>
                            <div class="img"></div>
                        </div>
                        <i class="material-icons-outlined dwn">arrow_forward_ios</i>
                    </div>
                    {profModal && <div class="profile_modal" id='profile_modal'>
                        <a to={-1} class='a'><i class="material-icons-outlined">person</i> My Profile</a>
                        <a class='a'><i class="material-icons-outlined">payment</i> Deposit</a>
                        <a class='a'><i class="material-icons-outlined">sell</i> Sell</a>
                        <a class='a'><i class="material-icons-outlined">account_balance_wallet</i> Wallet</a>
                        <a class='a'><i class="material-icons-outlined">insert_drive_file</i> Transaction history</a>
                        <a class='a'><i class="material-icons-outlined">logout</i> Logout</a>

                    </div>
                    }
                </div>

            </div>
            <i class="i ii material-icons" id='i'>menu</i>
            <!--{/* <i class="x ii material-icons" id='x'>close</i> */}-->

        </nav>
    </header>
</template>

<style scoped>
* {
    /* outline: solid 1px greenyellow; */
}


.blog_head nav {
    width: 100%;
    /* height: 89px; */
    /* border-bottom: solid 1px silver; */
    display: flex;
    justify-content: left;
    align-items: center;
    padding: 0 7%;
    /* position: fixed;  */
    /* top: 0;  */
    z-index: 5;
    /* overflow: hidden; */
}

.logo {
    height: 55px;
    width: 55px;
    margin: 0;
}

.logo_a {
    margin-right: 40px;
    display: flex;
    align-items: center;
}

.sp {}

.sp .link {
    margin: 0 15px;
    color: #1f1f1f;
    font-size: 16px;
    font-weight: 400;

}

.sp .link:hover {
    color: #2F67FA;
}

.log {
    margin-left: auto;
}

.log .link {
    padding: 9px 24px;
    border-radius: 30px;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
}

.login {
    color: #2F67FA;
    margin-right: 20px;
    font-weight: 500;
}

.signup {
    /* border: solid 1px silver; */
    /* background-color: #2F67FA; */
    background-color: #2F67FA;
    color: white;
    font-size: 16px;
}

.signup:hover {
    background-color: rgb(37, 150, 190, 0.8);
}

/* .material-icons{
    display: none;
} */

.i {
    display: none !important;
    /* border: solid; */
}

.x {
    margin-left: auto;
    display: none !important;
    color: #2F67FA;
}

nav .user {
    margin-left: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav .user .n_icon {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    /* border: solid; */
    height: fit-content;
    width: fit-content;
    width: 20px;
    height: 25px;
    margin-right: 30px;
    cursor: pointer;
}

nav .user .n_icon .bell {
    color: #7C859D;
    font-size: 26px;
    position: absolute;
}

nav .user .n_icon .not {
    width: 10px;
    height: 10px;
    border-radius: 100%;
    background-color: red;
    margin: 0 0 auto auto;
    position: relative;
    border: solid 2px white;
}

nav .user .profile {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    position: relative;
}

nav .user .profile .prof {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: fit-content;
    position: relative;

}

nav .user .profile .profile_modal {
    width: 100%;
    height: fit-content;
    /* border: solid; */
    background-color: white;
    border-radius: 15px;
    box-shadow: 0 0 8px 2px rgba(107, 107, 107, 0.07);
    position: absolute;
    top: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: 7px;
    row-gap: 10px;
    /* display: none; */
}

nav .user .profile .profile_modal .a {
    width: 100%;
    border-radius: 10px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: left;
    height: 50px;
    transition: 200ms;
    gap: 10px;
    padding: 0 13px;
    color: #373D4A;
    font-size: 15px;
    /* border: solid; */
}

nav .user .profile .profile_modal .a:hover {
    background-color: rgba(132, 131, 131, 0.1);
}

nav .user .profile .profile_modal .a i {
    font-size: 32px;
    font-weight: 200;
    color: #7C859D;
    /* border: solid; */
}

nav .user .user_descrpt {
    /* border: solid; */
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    row-gap: 3px;
    cursor: pointer;
}

nav .user .user_descrpt .username {
    font-weight: 500;
    font-size: 16px;
}

nav .user .user_descrpt .usermail {
    font-weight: 400;
    font-size: 14px;
    color: #7C859D;
}

nav .user .userimage {
    width: 42px;
    height: 42px;
    border-radius: 100%;
    margin-left: 20px;
    background-color: rgba(0, 0, 0, 0.07);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    cursor: pointer;
}

nav .user .userimage .me {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    border-radius: 100%;
    font-size: 14px;
    font-weight: 500;
    color: white;
    background-color: #5FA6F9;
    position: absolute;
}

nav .user .userimage .img {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    border-radius: 100%;
    position: relative;
    /* background-image: url('./images/country_image\ \(1\).svg'); */
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

nav .user .dwn {
    margin-left: 8px;
    rotate: 90deg;
    font-weight: 300;
    font-size: 18px;
    cursor: pointer;
}


.disp_none {
    /* display: none !important; */
}


@media screen and (min-width: 1300px) {
    nav {
        /* padding: 0 5%; */
        /* border: solid; */
    }
}

@media screen and (max-width: 1100px) {
    nav {
        padding: 0 5%;
    }
}

@media screen and (max-width: 1000px) {
    /* nav{
        padding: %;   
    } */

    .sp {
        display: none;
    }

    .log {
        margin-right: auto;
    }



    .i {
        color: #2F67FA;
        display: flex !important;
    }

    nav .user .dwn {
        margin-left: 8px;
        rotate: 90deg;
        font-weight: 300;
        font-size: 18px;
        cursor: pointer;
        margin-right: 40px;
    }
}

@media screen and (max-width: 600px) {
    nav {
        padding: 0 7%;
    }

    .logo_a {
        margin-right: auto;
    }

    .log {
        display: none;
    }

    .i {
        color: white;
        background-color: #2F67FA;
        border-radius: 100%;
        padding: 10px;
        font-size: 16px !important;
        display: flex !important;
    }

    nav .user .n_icon {
        margin-right: 25px;
    }

    nav .user .user_descrpt {
        display: none;
    }

    nav .user .userimage {
        display: none;
    }

    nav .user .dwn {
        display: none;
    }
}</style>