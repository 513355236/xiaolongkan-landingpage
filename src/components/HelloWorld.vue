<template>
  <div style="background: #a52321;">
    <div style="min-height: 100vh;display: flex;justify-content: center; align-items: center;padding: 4%;">
      <div class="card" v-if="!changeStatus">
        <h2 style="font-size: x-large;word-break: break-all;">❓ 退订确认</h2>
        <div class="row" style="margin-top: 32px;">
          <div class="label">门店信息</div>
        </div>
        <div style="display: flex;justify-content: space-between;font-size: 14px; align-items: center; border-bottom: none; " class="row">
          <div>
            <div style="font-weight: bold;font-size: 16px;" class="line">SOOLOONGKAN Berlin</div>
            <div style="margin-top:16px;"  class="line">
              <a
                  style="color: black;"
                  href="https://www.google.com/maps/place/ShooLoongKan+HotPot+%E5%B0%8F%E9%BE%99%E5%9D%8E+%E8%80%81%E7%81%AB%E9%94%85+Chinese+Fondue/@52.5016362,13.3271184,17z/data=!3m1!4b1!4m5!3m4!1s0x47a851abd92a6693:0xbdc31d2fe47ed24d!8m2!3d52.5016381!4d13.3292134">
                📍 MeinekeStraße 22, 10719 Berlin</a>

            </div>
            <div class="line"><a     style="color: black;" href="tel://00493061293515">☎️ 03061293515</a></div>
            <div class="line">🕑 12:00-23:00</div>

          </div>
          <div>
            <img :src="logo2" width="96">
          </div>
        </div>
        <div class="row" style="margin-top: 64px;">
          <div class="label">退订信息</div>
        </div>
        <div class="row">
          <div class="label">退订人:</div>
          <div class="value"> xx </div>
        </div>
        <div class="row">
          <div class="label">退订时间:</div>
          <div class="value">   dd.mm.yy hh.mm   </div>
        </div>
        <div class="row" style="justify-content: center;flex-direction: column; align-items: center;text-align: center;">
          <img :src="logo1" width="128">
          <p>
            Nothing can be solved by a Hotpot. <br>
            If so, just <b>ShooLoongKan Berlin</b>.
          </p>
        </div>
        <div class="row" style="justify-content: center;flex-direction: column; align-items: center;text-align: center;">
          <el-button type="danger" @click="changeStatus=!changeStatus">确认退订</el-button>
        </div>
      </div>

      <div class="card" v-else>
        <h2 style="font-size: x-large;word-break: break-all;">✔️ 退订成功</h2>
        <div class="row" style="margin-top: 32px;">
          <div class="label">门店信息</div>
        </div>
        <div style="display: flex;justify-content: space-between;font-size: 14px; align-items: center; border-bottom: none; " class="row">
          <div>
            <div style="font-weight: bold;font-size: 16px;" class="line">SOOLOONGKAN Berlin</div>
            <div style="margin-top:16px;"  class="line">
              <a
                  style="color: black;"
                  href="https://www.google.com/maps/place/ShooLoongKan+HotPot+%E5%B0%8F%E9%BE%99%E5%9D%8E+%E8%80%81%E7%81%AB%E9%94%85+Chinese+Fondue/@52.5016362,13.3271184,17z/data=!3m1!4b1!4m5!3m4!1s0x47a851abd92a6693:0xbdc31d2fe47ed24d!8m2!3d52.5016381!4d13.3292134">
                📍 MeinekeStraße 22, 10719 Berlin</a>

            </div>
            <div class="line"><a     style="color: black;" href="tel://00493061293515">☎️ 03061293515</a></div>
            <div class="line">🕑 12:00-23:00</div>

          </div>
          <div>
            <img :src="logo2" width="96">
          </div>
        </div>
        <div class="row" style="margin-top: 64px;">
          <b>欢迎下次光临！</b>
        </div>
        <div class="row" style="justify-content: center;flex-direction: column; align-items: center;text-align: center;">
          <img :src="logo1" width="128">
          <p>
            Nothing can be solved by a Hotpot. <br>
            If so, just <b>ShooLoongKan Berlin</b>.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      logo1: require('@/assets/logo.jpg'),
      logo2: require('@/assets/logo2.png'),
      changeStatus: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card{
  border-radius: 24px;
  background: white;
  max-width: 496px;
  flex-shrink: 1;
  width: 464px;
  margin: auto;
  padding: 24px;
}
.row{
  display: flex;
  justify-content: space-between;
  padding: 8px 0 12px 0;
  border-bottom: 1px dashed gainsboro;
  margin-top: 16px;
}
.row .label{
  font-weight: bold;
}
.line{
  margin-top: 2px;
  padding: 2px 0;
}
table {margin:auto;}
</style>
