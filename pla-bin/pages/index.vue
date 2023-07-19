<template>
    <div>
        <!-- Card msg -->
        <div class="card">
            <div class="grid-card" v-for="data in postdata" :key="data.id" >
                <div class="h-card">                    
                    <div class="userpost">                                              
                        <h3 style="justify-content: left; display: flex; margin-left: 3%;" ><img src="imgs/user.png" style="width: 40px; height: 40px;" alt="">{{ data.user }}<p>{{ data.timestamp }}</p></h3>                      
                    </div>
                </div>            
                <div class="c-card">
                    <p>{{ data.msg }}</p>
                </div>
                <div class="f-card">
                    <button class="btn-like" >❤️</button>
                    <button class="btn-dislike" >😒</button>                  
                    <input id="comment" type="text" placeholder="แสดงความคิดเห็น">
                    <button class="btn-sendmsg" >✉️</button>
                </div> 
            </div> 
            
            
        </div>
        <!-- End Card msg -->                
    </div>
</template>

<script>
export default {
    data() {
        return {
            postdata: [
            {   id: 1,
                user: 'Seepair',
                msg: 'ปล่อยกางเกงจ้าา เอว 28',
                timestamp: 'พุธ 19 กรกฏาคม 66'
            },
            {   id: 2,
                user: 'Tle',
                msg: 'หาตี้คืนนี้ครับ',
                timestamp: 'พุธ 19 กรกฏาคม 66'
            },
            {   id: 3,
                user: 'Film',
                msg: 'พัทยาทักครับบบบ',
                timestamp: 'พุธ 19 กรกฏาคม 66'
            },
            {   id: 4,
                user: 'Film',
                msg: 'ยันเช้าคืนนี้',
                timestamp: 'พุธ 19 กรกฏาคม 66'
            },
            {   id: 5,
                user: 'Goiii',
                msg: 'หาตี้วาโล แพท++ ขาด2',
                timestamp: 'พุธ 18 กรกฏาคม 66'
            },
            {   id: 6,
                user: 'Tle',
                msg: 'อยากตกปลาาาา ใครว่างไปด้วยหน่อย',
                timestamp: 'พุธ 18 กรกฏาคม 66'
            },
        ]
        }
    }
        
}
</script>

<style scoped>
.card{
    display: grid;
    grid-template-rows: 1fr 1fr 1fr;
    width: 100%;
    height: 18.125rem;
    background-color: #E6F9FF;
    margin-bottom: 5px;
    text-align: center;
    box-shadow: rgba(9, 30, 66, 0.25) 0px 1px 1px, rgba(9, 30, 66, 0.13) 0px 0px 1px 1px;
}
.c-card {
    justify-content: left;
    display: flex;
    width: 100%;
    height: 100%;
    background-color: #E6F9FF;
    box-shadow: rgba(0, 0, 0, 0.06) 0px 2px 4px 0px inset;
    padding: 3%;
}
.h-card {
    height: 100%;
    background-color: #BFF1FF;
    box-shadow: rgba(9, 30, 66, 0.25) 0px 1px 1px, rgba(9, 30, 66, 0.13) 0px 0px 1px 1px;
}
.grid-card {
    display: grid;
    grid-template-rows: 0.5fr 2fr 0.5fr;
    box-shadow: rgba(9, 30, 66, 0.25) 0px 1px 1px, rgba(9, 30, 66, 0.13) 0px 0px 1px 1px;
}
.userpost p{
    padding: 2%;
    font-size: 12px;
    color: #60AABF;
}
.f-card {
    background-color: #E6F9FF;
}
.f-card input {
    border-radius: 14px;
    border: none;
    width: 60%;
    height: 60%;   
}
.f-card input:hover {
    border: 1px solid #80bbff;
    background-color: #80E3FF;
}
.btn-like{
    border-radius: 10px;
    border: none;
    background-color: #80e3ffbd; 
    margin: 1%;
    height: 60%;
    width: 10%;
}
.btn-like:hover {
    background-color: #fc06b2bd; 
}
.btn-dislike{
    border-radius: 10px;
    border: none;
    background-color: #80e3ffbd; 
    margin: 1%;
    height: 60%;
    width: 8%;
}
.btn-dislike:hover {
    background-color: #fc5406bd; 
}
.btn-sendmsg{
    border-radius: 10px;
    border: none;
    background-color: #80e3ffbd; 
    margin: 1%;
    height: 60%;
}
.btn-sendmsg:hover {
    background-color: #80bbff; 
}
</style>