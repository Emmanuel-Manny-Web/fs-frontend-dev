<template>
    <div>
        <!--<AddNew />-->
        <InternalHeader />
        <main class="blg_main">
            <section class="sectionprof_top">
                <p class="p1">My Profile</p>
                <p class="p2">User ID: <span>TNF/82T38RT904-01</span></p>
            </section>
            <section class="sectionfin_stck">
                <div class="bck">
                    <img src="" alt="" />
                </div>
                <section class="mn">
                    <NameProfile />
                    <p class="t4"> Trade Smart, Simple and Easy! </p>
                </section>
            </section>

            <section class="sectionprof_input">
                <form action="" class='prof_form'>
                    <label htmlFor="" class='in_s'>
                        First name
                        <input type="text" placeholder='Enter your first name' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Last name
                        <input type="text" placeholder='Last name' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Other name
                        <input type="text" placeholder='Other name' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Preferred username
                        <input type="text" placeholder='Username' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Email
                        <input type="text" placeholder='Example@gmail.com' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Phone number
                        <input type="text" placeholder='70948209' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Nationality
                        <input type="text" placeholder='Select country' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Country of residence
                        <input type="text" placeholder='Select country' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        State / province / region
                        <input type="text" placeholder='Select country' />
                    </label>
                    <label htmlFor="" class='in_s'>
                        Local Government Area
                        <input type="text" placeholder='Select country' />
                    </label>

                    <label htmlFor="" class='in_s in_l'>
                        Residential address
                        <input type="text" placeholder='Residential address' />
                    </label>

                    <button type="submit" class='a'>Save Changes</button>

                </form>
                <div class="crds">
                    <div class="crd">
                        <a class='a'>
                            <img src="" alt="" />
                            <span class="sp">
                                <p>Wallet</p>
                                <i class='material-icons'>arrow_forward_ios</i>
                            </span>
                        </a>
                        <a class='a'>
                            <img src="" alt="" />
                            <span class="sp">
                                <p>Transactions</p>
                                <i class='material-icons'>arrow_forward_ios</i>
                            </span>
                        </a>
                        <a class='a'>
                            <img src="" alt="" />
                            <span class="sp">
                                <p>Ad list</p>
                                <i class='material-icons'>arrow_forward_ios</i>
                            </span>
                        </a>
                    </div>


                </div>
            </section>
            <section class="section_accts">
                <p class="save">
                    Saved accounts
                <p class="p1">
                <p class='spp'>+</p> Add new</p>
                </p>


                <!--<div class="accts">
              <Account_info_crd img={bank2} acct_name={'Peter Williams'} acct_no={'40196789894'} acct_currency={'USD'} />
              <Account_info_crd img={bank1} acct_name={'Peter Williams'} acct_no={'40196789894'} acct_currency={'USD'} />
              <Account_info_crd img={bank2} acct_name={'Peter Williams'} acct_no={'40196789894'} acct_currency={'USD'} />
              <Account_info_crd img={bank1} acct_name={'Peter Williams'} acct_no={'40196789894'} acct_currency={'USD'} />
              <Account_info_crd img={bank2} acct_name={'Peter Williams'} acct_no={'40196789894'} acct_currency={'USD'} />
              <Account_info_crd img={bank1} acct_name={'Peter Williams'} acct_no={'40196789894'} acct_currency={'USD'} />
          </div>-->
            </section>
        </main>

        <ExternalFooter />
    </div>
</template>

<style scoped>
.blg_main .sectionprof_top {
    justify-content: space-between;
    align-items: center;
    margin-top: 25px;
}

.blg_main .sectionprof_top .p1 {
    font-size: 20px;
    font-weight: 700;
    font-family: 'lora', sans-serif;
    color: #373D4A;
}

.blg_main .sectionprof_top .p2 {
    font-size: 16px;
    font-weight: 400;
    color: #373D4A;
}

.blg_main .sectionprof_top .p2 span {
    font-size: 17px;
    font-weight: 700;
    margin-left: 20px;
    color: #18191B;
}

.blg_main .sectionfin_stck {
    height: 100px;
    width: 100%;
    margin: 25px 0;
    background-color: #EBF0FF;
    position: relative;
}

.blg_main .sectionfin_stck {
    height: fit-content;
    width: 100%;
    margin: 25px 0;
    position: relative;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: right;
    padding: 15px 0;
}

.blg_main .sectionfin_stck .bck {
    background-color: #EBF0FF;
    position: absolute;
    /* width: 100%; */
    height: 100%;
    display: flex;
    align-items: center;
    /* justify-content: right; */
    /* margin-right: 0; */
    /* margin-left: auto; */
    /* border: solid; */
}

.blg_main .sectionfin_stck .bck img {
    /* transform: matrix(-1, 0, 0, 1, 0, 0); */
    height: 100%;
}

.blg_main .sectionfin_stck .mn {
    position: relative;
    width: 100%;
    height: 100%;
    /* border: solid; */
    display: flex;
    justify-content: space-between;
    align-items: center;
}


.blg_main .sectionfin_stck .mn .t4 {
    font-size: 24px;
    font-family: 'sofia', cursive;
    color: #2F67FA;
    width: 300px;
    text-align: right;
}

.blg_main .sectionprof_input {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: space-between;
    width: 100%;
    gap: 45px;
}

.blg_main .sectionprof_input .crds {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    justify-content: flex-start;
    width: fit-content;
    /* border: solid; */
    /* height: fit-content; */
    gap: 15px;
    row-gap: 25px;
    /* overflow: scroll; */

}

.blg_main .sectionprof_input .crds .crd {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    justify-content: flex-start;
    width: fit-content;
    gap: 15px;
    row-gap: 25px;
}

.blg_main .sectionprof_input .crds .a {
    width: 300px;
    height: 130px;
    border: solid 1.5px #C5C9D3;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    row-gap: 20px;
    padding: 0 25px;
    color: #373D4A;
}

.blg_main .sectionprof_input .crds .a:hover {
    background-color: #F9FAFB;
}

.blg_main .sectionprof_input .crds .i1 {
    font-size: 65px;
    /* border: solid; */
}

.blg_main .sectionprof_input .crds .a img {
    width: 40px;
    height: 40px;
}

.blg_main .sectionprof_input .crds .a .sp {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
}

.blg_main .sectionprof_input .crds .a .sp p {
    font-family: 'lora', sans-serif;
    font-weight: 700;
}

.blg_main .sectionprof_input .crds .a .sp i {
    color: #7C859D;
}




.blg_main .sectionprof_input form {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: space-between;
    width: 100%;
    gap: 25px;
    /* row-gap: 20px; */
    flex-wrap: wrap;
}

.blg_main .sectionprof_input form .in_s {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;
    width: 48%;
    /* border: solid; */
    row-gap: 10px;
    margin-bottom: 15px;
}

.blg_main .sectionprof_input form .in_l {

    width: 100%;

}


.blg_main .sectionprof_input form .in_s input {
    width: 100%;
    height: 100%;
    border-radius: 30px;
    border: solid 1px #DCDEE5;
    height: 55px;
    padding: 0 20px;
    outline: none;
}

.blg_main .sectionprof_input form .in_s input:focus {
    background-color: #F9FAFB;
}

.blg_main .sectionprof_input form .in_s input::placeholder {
    color: #7C859D;
}

.blg_main .sectionprof_input form .a {
    height: 50px;
    border-radius: 48px;
    color: white;
    background-color: #2F67FA;
    font-weight: 600;
    border: none;
    padding: 0 35px;
    font-size: 16px;
}

.blg_main .section_accts {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    margin-top: 5%;
}

.blg_main .section_accts .save {
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    color: #18191B;
    font-size: 20px;
    font-family: 'lora', sans-serif;
    font-weight: 700;
}

.blg_main .section_accts .save .p1 {
    color: #2F67FA;
    font-size: 17px;
    font-family: 'open sans', sans-serif;
    font-weight: 600;
    display: flex;
    align-items: center;
    cursor: pointer;
}

.blg_main .section_accts .save .p1 .spp {
    color: #2F67FA;
    margin-right: 10px;
    font-size: 20px;
    font-weight: 800;
}

.blg_main .section_accts .accts {
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    row-gap: 15px;

    justify-content: left;
    margin-top: 30px;
    gap: 3%;
    /* column-gap: 20px; */
    row-gap: 35px;
    flex-wrap: wrap;
    /* border: solid; */
}

.blg_main .section_accts .accts .act {
    border: solid 1px #DCDEE5;
    border-radius: 10px;
    height: 90px;
    width: 31%;
    /* max-width: 400px; */
    display: flex;
    align-items: center;
    justify-content: left;
    padding: 0 15px;
}

.blg_main .section_accts .accts .act .txt {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-direction: column;
    row-gap: 6px;
    margin-left: 10px;
}

.blg_main .section_accts .accts .act .txt .p1 {
    font-size: 16px;
    color: #373D4A;
    font-weight: 600;
}

.blg_main .section_accts .accts .act .txt .p2 {
    font-size: 14px;
    color: #7C859D;
    font-weight: 600;
    display: flex;
    align-items: center;
}

.blg_main .section_accts .accts .act .txt .p2 .ct::after {
    /* border: solid; */
    /* border-radius: 100%; */
    margin: 0 010px;
    content: '\2022';
}

.blg_main .section_accts .accts .act i {
    margin-left: auto;
    font-size: 30px;
    color: #7C859D;
    font-weight: 300;
}




@media screen and (max-width: 1150px) {
    .blg_main .sectionprof_top {
        padding: 0 7%;
    }


    .blg_main .sectionprof_top .p1 {
        font-size: 16px;
    }

    .blg_main .sectionprof_top .p2 {
        font-size: 12px;
    }

    .blg_main .sectionprof_top .p2 span {
        font-size: 14px;
        margin-left: 5px;
    }

    .blg_main .sectionfin_stck .mn .t4 {
        /* font-size: 0px */
        /* width: 330px; */
    }

    .blg_main .sectionprof_input {
        flex-direction: column;
    }

    .blg_main .sectionprof_input .crds {
        order: 1;
        width: 100%;
        flex-direction: row;
        /* overflow: scroll; */
        /* border: solid; */
        /* border: solid; */
        /* margin: 0; */
    }

    .blg_main .sectionprof_input .crds .crd {
        order: 1;
        width: fit-content;
        flex-direction: row;
        /* overflow: scroll; */
        /* border: solid; */
        flex-wrap: wrap;
    }


    .blg_main .sectionprof_input .crds .a {
        width: 180px;
        height: 80px;
        padding: 15px;
        row-gap: 10px;
    }

    .blg_main .sectionprof_input .crds .a img {
        width: 20px;
        height: 20px;
    }

    .blg_main .sectionprof_input .crds .a .sp p {
        font-size: 14px;
    }

    .blg_main .sectionprof_input .crds .a .sp i {
        color: #7C859D;
        font-size: 20px;
    }


    .blg_main .sectionprof_input form {
        order: 2;
        margin-top: 0px;
        /* border: solid; */
    }

    .blg_main .section_accts .accts {
        gap: 10%;
        row-gap: 25px;
        flex-wrap: wrap;
    }

    .blg_main .section_accts .accts .act {
        width: 45%;
    }

}

@media screen and (max-width: 1100px) {
    .blg_main .sectionprof_top {
        padding: 0 5%;
    }
}

@media screen and (max-width: 1000px) {
    .blg_main .sectionfin_stck {
        padding: 10px 0;
    }

}




@media screen and (max-width: 1000px) {
    .blg_main .sectionfin_stck {
        padding: 10px 0;
    }

    .blg_main .sectionfin_stck .mn .t4 {
        font-size: 24px;
        width: 300px;
    }

    .blg_main .section_accts .accts {
        gap: 6%;
        row-gap: 25px;
        flex-wrap: wrap;
    }

    .blg_main .section_accts .accts .act {
        width: 47%;
    }
}


@media screen and (max-width: 730px) {
    .blg_main .sectionfin_stck {
        padding: 20px 0;
    }

    .blg_main .sectionfin_stck .mn .t4 {
        font-size: 20px;
        width: 180px;
        /* border: solid; */
    }

    .blg_main .sectionprof_input form {

        gap: 10px;

    }

    .blg_main .sectionprof_input form .in_s {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: space-between;
        width: 100%;
        font-size: 15px;

    }

    .blg_main .sectionprof_input form .in_s input {

        border-radius: 10px;

    }

    .blg_main .sectionprof_input .crds .crd {
        /* border: solid; */
        width: 100%;
    }

    .blg_main .sectionprof_input .crds .a {
        width: 46%;
        height: 80px;
        padding: 15px;
        max-width: 300px;
    }

    .blg_main .section_accts {
        margin-top: 50px;
    }

    .blg_main .section_accts .save {
        font-size: 16px;
        font-weight: 800;
    }

    .blg_main .section_accts .save .p1 {
        color: #2F67FA;
        font-size: 14px;
        font-family: 'open sans', sans-serif;
        font-weight: 600;
        display: flex;
        align-items: center;
        cursor: pointer;
    }

    .blg_main .section_accts .save .p1 .spp {
        margin-right: 8px;
        font-size: 18px;
        font-weight: 800;
    }

    .blg_main .section_accts .accts {
        gap: 6%;
        row-gap: 25px;
        flex-wrap: wrap;
    }

    .blg_main .section_accts .accts .act {
        width: 100%;
        height: 85px;
    }

    .blg_main .section_accts .accts .act img {
        width: 35px;
        height: 35px;
    }

    .blg_main .section_accts .accts .act i {
        font-size: 26px;
    }

    .blg_main .section_accts .accts .act .txt {
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        row-gap: 6px;
        margin-left: 13px;
    }

    .blg_main .section_accts .accts .act .txt .p1 {
        font-size: 15px;
        font-weight: 800;
    }

    .blg_main .section_accts .accts .act .txt .p2 {
        font-size: 14px;
    }
}


@media screen and (max-width: 600px) {
    .blg_main .sectionprof_top {
        padding: 0 7%;
    }

    .blg_main .sectionprof_top .p1 {
        font-size: 15px;
    }

    .blg_main .sectionprof_top .p2 span {
        font-size: 13px;
        margin-left: 2.5px;
    }

    .blg_main .sectionfin_stck {
        padding: 15px 0;
    }

    .blg_main .sectionfin_stck .mn .t4 {
        display: none;
    }



}</style>