<template>
    <div id="j-foot">
        <router-link to="/">
            <p ref="index"><img src="../../../svg/首页.svg" alt="" class="j-foot1"/><br /><span>首页</span></p>
        </router-link>
         <router-link to="/list">
            <p ref="list"><img src="../../../svg/分类.svg" alt="" class="j-foot2"/><br /><span>分类</span></p>
         </router-link>
         <router-link to="/car">
            <p ref="car"><img src="../../../svg/购物车空.svg" alt="" class="j-foot3"/><br /><span>购物车</span></p>
        </router-link>
        <router-link to="/my"> 
            <p ref="my"><img src="../../../svg/我的.svg" alt="" class="j-foot4"/><br /><span>我的</span></p>
        </router-link>
    </div>
</template>

<script type="text/javascript">
    import './foot.scss'
    export default{
        mounted(){
                // console.log(this.$router.history.current.path)
                if(this.$router.history.current.path=='/'){
                    // console.log(this.$refs.index);
                    this.$refs.index.classList.add('active');

                }else if(this.$router.history.current.path=='/list'){
                     this.$refs.list.classList.add('active');
                }else if(this.$router.history.current.path=='/car'){
                     this.$refs.car.classList.add('active');
                }else if(this.$router.history.current.path=='/my'){
                     this.$refs.my.classList.add('active');
                }

        }
    }



</script>