<template>
    <div class="container">
        <header class="h">
            <div class="headbar">
                <div class="nameapp" style="margin-left: 10%;">
                    <h3>PLA-BIN</h3>
                </div>
                <div class="displayname">
                                       
                </div>
                <div class="img-user">
                    <p><strong>{{ userlogin }}</strong></p>
                    <img src="imgs/user.png" alt="" style="width: 50px; height: 50px; ">
                    
                </div>
            </div>
        </header>
        <div>
            <slot/>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            userlogin: 'Joe'
        }
    }        
}
</script>

<style>
.headbar {
    background-color: #80E3FF;
    width: 100%;
    height: 30%;
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    color: aliceblue;
    margin-bottom: 3px;
    box-shadow: rgba(9, 30, 66, 0.25) 0px 1px 1px, rgba(9, 30, 66, 0.13) 0px 0px 1px 1px;
    
}
.h {
    
    position: sticky;
    top: 0px;
}
.displayname {
    text-align: right;
    display: flex;   
    justify-content: right;   
    font-size: large;
}
.img-user {
    text-align: right;
    display: flex;   
    justify-content: center;
    margin: 5%;
}
body {
    margin: 0px;
    padding: 0px;
}
* {
    font-family: 'Mitr', sans-serif;
    font-weight: 200;
}


</style>