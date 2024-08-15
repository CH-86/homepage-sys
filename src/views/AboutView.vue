<script setup>
import ContList from '../components/ContList.vue'
import ContentsOfService from '../components/ContentsOfService.vue'
</script>

<template>
  <div class="about">
    <div>
      <el-descriptions title="&nbsp;会社概要" column="1" border size="small">
        <el-descriptions-item label="商号">株式会社エス・ティ・エス </el-descriptions-item>
        <el-descriptions-item label="代表取締役">内藤 照雄</el-descriptions-item>
        <el-descriptions-item label="設立">平成１３年１月１５日 </el-descriptions-item>
        <el-descriptions-item label="事業開始">平成１３年２月１日 </el-descriptions-item>
        <el-descriptions-item label="沿革"
          >平成１８年８月１日<br />有限会社システムトータルサービスより<br />商号変更
        </el-descriptions-item>
        <el-descriptions-item label="資本金	">１，０００万円 </el-descriptions-item>
        <el-descriptions-item label="本店	">東京都中央区勝どき 2-18-1 </el-descriptions-item>
        <el-descriptions-item label="開発センター		"
          >東京都台東区東上野1-24-2 <br />山茂ビル 2F<br />TEL：03-5807-8691<br />FAX：03-5807-8692
        </el-descriptions-item>
        <div>1231</div>
        <el-descriptions-item>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12958.93565690631!2d139.779653!3d35.708165!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60188ea2136915a5%3A0xc1f4112021c1be84!2z5bGx6IyC44OT44Or!5e0!3m2!1sja!2sus!4v1723614288747!5m2!1sja!2sus"
            width="300"
            height="200"
            style="border: 0"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </el-descriptions-item>
        <el-descriptions-item label="事業内容		">
          1. コンピュータシステムの受託開発<br />2. コンピュータシステムのｱｳﾄｿｰｼﾝｸﾞ <br />3.
          コンピュータのパッケージサービス<br />4. コンピュータに関するコンサルティング<br />5.
          コンピュータ技術者の派遣 <br />6. メンタルヘルス事業
        </el-descriptions-item>
        <el-descriptions-item label="取引銀行	">
          東日本銀行&nbsp;月島支店<br />三菱東京ＵＦＪ銀行&nbsp;上野支店
        </el-descriptions-item>
        <el-descriptions-item label="ビジネスパートナー	"> 株式会社MD.ネット </el-descriptions-item>
        <el-descriptions-item label="主な取引先	">
          株式会社アクロネット<br />株式会社アドブ <br />
          アルファ インフォメーション ソリューション株式会社<br />株式会社エイジア <br />
          株式会社工芸精器製作所<br />株式会社システム・ナビゲート
          <br />株式会社ソルパック<br />株式会社ネオテックス<br />株式会社ベーネットシステムズ<br />株式会社ワールドリブメーション<br />他
        </el-descriptions-item>
      </el-descriptions>
    </div>
  </div>
  <div style="width: 380px">
    <ContList />
    <ContentsOfService />
  </div>
</template>

<style>
.el-descriptions__label {
  width: 60px;
}
.about {
  width: 380px;
}
</style>
