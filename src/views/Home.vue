<template>
    <div class="home">

        <van-stepper v-model="value1" />
        <div>{{val}}</div>


        <!-- <van-button type="primary" @click="fal">主要按钮</van-button> -->
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Vue from "vue";
import { Popup,Field ,Stepper,Cell,Toast,Button} from "vant";

Vue.use(Popup).use(Field).use(Stepper).use(Cell).use(Toast).use(Button);

export default {
    name: "Home",
    components: {
        HelloWorld,
    },
    data() {
        return {
            show: false,
            value:'',
            value1: 1,
            d:5
        };
    },

    methods: {
        showPopup() {
            this.show = true;
        },
        fal(){
            Toast.success('成功文案');
        },
    },
    computed:{
        val:function(){
            return this.value1 + this.d
        }
    }
};
</script>
