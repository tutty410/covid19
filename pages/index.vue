<template>
  <div class="MainPage">
    <site-top-upper />
    <cards-tabs />
    <card-row class="DataBlock">
      <!-- 検査陽性者の状況 -->
      <confirmed-cases-details-card />
      <!-- 新規患者に関する報告件数の推移 -->
      <confirmed-cases-number-card />
      <!-- モニタリング指標 -->
      <monitoring-status-overview-card />
      <!-- モニタリング(1)新規陽性者数 -->
      <monitoring-confirmed-cases-number-card />
      <!-- モニタリング指標(2)新規陽性者における接触歴等不明率 -->
      <untracked-rate-card />
      <!-- モニタリング指標(3)週単位の陽性者増加比 -->
      <confirmed-cases-increase-ratio-by-week-card />
      <!-- モニタリング指標(4)重症患者数 -->
      <severe-case-card />
      <!-- モニタリング指標(5)入院患者数 -->
      <hospitalized-number-card />
      <!-- モニタリング指標(6)PCR検査の陽性率-->
      <positive-rate-card />
      <!-- モニタリング指標(7)受診相談窓口における相談件数 -->
      <monitoring-consultation-desk-reports-number-card />
    </card-row>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import SiteTopUpper from '@/components/SiteTopUpper.vue'
import CardsTabs from '@/components/CardsTabs.vue'
import CardRow from '@/components/cards/CardRow.vue'
import ConfirmedCasesDetailsCard from '@/components/cards/ConfirmedCasesDetailsCard.vue'
import ConfirmedCasesNumberCard from '@/components/cards/ConfirmedCasesNumberCard.vue'
import MonitoringConfirmedCasesNumberCard from '@/components/cards/MonitoringConfirmedCasesNumberCard.vue'
import PositiveRateCard from '~/components/cards/PositiveRateCard.vue'
import SevereCaseCard from '@/components/cards/SevereCaseCard.vue'
import UntrackedRateCard from '@/components/cards/UntrackedRateCard.vue'
import ConfirmedCasesIncreaseRatioByWeekCard from '@/components/cards/ConfirmedCasesIncreaseRatioByWeekCard.vue'
import HospitalizedNumberCard from '@/components/cards/HospitalizedNumberCard.vue'
import MonitoringStatusOverviewCard from '@/components/cards/MonitoringStatusOverviewCard.vue'
import MonitoringConsultationDeskReportsNumberCard from '@/components/cards/MonitoringConsultationDeskReportsNumberCard.vue'

export default Vue.extend({
  components: {
    SiteTopUpper,
    CardsTabs,
    CardRow,
    MonitoringConfirmedCasesNumberCard,
    UntrackedRateCard,
    SevereCaseCard,
    MonitoringConsultationDeskReportsNumberCard,
    PositiveRateCard,
    ConfirmedCasesDetailsCard,
    ConfirmedCasesNumberCard,
    ConfirmedCasesIncreaseRatioByWeekCard,
    HospitalizedNumberCard,
    MonitoringStatusOverviewCard
  }
})
</script>

<style lang="scss" scoped>
.MainPage {
  .DataBlock {
    margin: 20px -8px;

    .DataCard {
      @include largerThan($medium) {
        padding: 10px;
      }

      @include lessThan($small) {
        padding: 4px 8px;
      }
    }
  }
}
</style>
