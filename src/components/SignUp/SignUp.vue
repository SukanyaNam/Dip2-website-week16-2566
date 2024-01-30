<script setup>
import { reactive } from 'vue';
import { useRoute } from 'vue-router';

const router = useRoute()
const userform = reactive({
    fname: "",
    lname: "",
    email: "",
    password: "",
    phone: "",
    address: "",
});
function SignInPage() {
    router.push({ name: "signin" })
}
</script>


<template>
    <div class="container mt-4">
        <div class="row">
            <div class="col-md-5 mb-1">
                <div class="card shadow">
                    <div class="card-header p-0">
                        <img src="https://cdn.pixabay.com/photo/2014/08/12/17/00/india-416777_640.jpg"
                            class="card-img-top" alt="sign">
                    </div>
                    <div class="card-body">
                        <p class="card-text text-end">สิ่งมหัศรรย์ของโลก 2024.</p>
                    </div>
                </div>
            </div>
            <div class="col-md-7">
                <div class="card shadow ">
                     <div class="card shadow ">
                        <div class="card-header p-0 bg-danger text-light">
                            <h5>ระบบลงทะเบียนผู้ใช้งาน</h5>
                        </div>
                        <div class="card-body">
                            <form action="">
                                <div class="mb-2">
                                    <label for="" class="form-label" >ชื่อ</label>
                                    <input type="text" class="form-control" v-model="userform.fname" placeholder="ชื่อผู้สมัคร" required>
                                </div>

                                 <div class="mb-2">
                                    <label for="" class="form-label" >นามสกุล</label>
                                    <input type="text" class="form-control" v-model="userform.lname" placeholder="นามสกุลผู้สมัคร" required>
                                 </div>

                                 <div class="mb-2">
                                    <label for="" class="form-label">อีเมล</label>
                                    <input type="email" class="form-control"  v-model="userform.email" placeholder="อีเมลผู้สมัคร" required>
                                </div>

                                <div class="mb-2">
                                    <label for="" class="form-label" >รหัสผ่าน</label>
                                    <input type="password" class="form-control" v-model="userform.password" placeholder="รหัสผ่านผู้สมัคร" required>
                                </div>

                                <div class="mb-2">
                                     <label for="" class="form-label">เบอร์โทรศัพท์</label>
                                    <input type="text" class="form-control" v-model="userform.phone" placeholder="เบอร์โทรศัพท์ผู้สมัคร" required>
                                </div>

                                <div class="mb-2">
                                    <label for="" class="form-label">ที่อยู่</label>
                                    <input type="text" class="form-control" v-model="userform.address" placeholder="ที่อยู่ผู้สมัคร">
                                    <textarea name="ที่อยู่" id="" cols="61" rows="2"></textarea>
                                </div>
                                <p type="button" class="btn btn-danger d-block">สมัครสมาชิก</p>
                                 <p @click="SignInPage" class="btn btn-danger shadow d-block" >
                                        Already have an Account?
                                        <router-link :to="{ name: 'signin' }">
                                            Sing In
                                        </router-link>
                                    </p>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Sarabun&display=swap');

.container {
    font-family: 'Sarabun', sans-serif;
    
}
.form-label {
    color: rgb(6, 96, 0);
}
</style>