<template>
  <el-container class="index-el-container">
    <!--    头部布局-->
    <el-header>
      <div class = 'header-div'>
        <img class="header-img" src="../assets/logo.png">
        <span>Admin</span>
      </div>

      <div class="header-div-information">
        <el-button type="info" >退出</el-button>
      </div>
    </el-header>

    <el-container>
      <!--      侧边栏布局-->
      <el-aside width="200px">

        <el-menu default-active="2" class="el-menu-vertical-demo" background-color="#333744" text-color="#fff" active-text-color="#ffd04b">

          <el-menu-item index="1">
            <i class="el-icon-menu"></i>
            <span slot="title">导航一</span>
          </el-menu-item>
          <el-menu-item index="2" disabled>
            <i class="el-icon-document"></i>
            <span slot="title">导航二</span>
          </el-menu-item>
          <el-menu-item index="3">
            <i class="el-icon-setting"></i>
            <span slot="title">设置</span>
          </el-menu-item>
        </el-menu>

      </el-aside>
      <el-container>
        <!--        主页面-->
        <el-main>Main</el-main>
        <!--        底部-->
        <el-footer>Footer</el-footer>
      </el-container>
    </el-container>
  </el-container>
</template>

<script>



    export default {
        created() {
          this.getMenuList()
        },
        methods: {
            getMenuList(){
              this.$http.get('/getMemuList')
            },
        },
        data() {
            const item = {
                date: '2016-05-02',
                name: '王小虎',
                address: '上海市普陀区金沙江路 1518 弄'
            };
            return {
                tableData: Array(20).fill(item),
                account: '陈洋',
                password: '123'
            }
        }
    };
</script>

<style lang="less" scoped>
  .index-el-container{
    height: 100%;
  }
  .el-header {
    background-color: #373d41;
    color: #fff;
    text-align: center;
    line-height: 60px;
    display: flex;
    justify-content: space-between;
    padding-left: 0px;
    align-items: center;
    font-size: 20px;




  }

  .header-div{
    display: flex;
  }
  .header-img{
    width: 50px;
    height: 50px;
  }


  .el-footer {
    background-color: #373d41;
    color: #fff;
    text-align: center;
    line-height: 60px;
  }

  .el-aside {
    background-color: #333744;
    color: #fff;
    text-align: left;
    line-height: 200px;
  }

  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: left;
    line-height: 160px;
  }

  body > .el-container {
    margin-bottom: 40px;
  }

  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }

  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>

