<template>
  <ContentWrap>
    <doc-alert title="报表设计器" url="https://doc.iocoder.cn/report/" />

    <IFrame :src="src" />
  </ContentWrap>
</template>
<script lang="ts" setup>
import { getAccessToken } from '@/utils/auth'

defineOptions({ name: 'JimuReport' })

const BASE_URL = import.meta.env.VITE_BASE_URL
const src = ref(BASE_URL + '/jmreport/list?token=' + getAccessToken())
</script>
