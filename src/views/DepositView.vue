<script setup>
import DepositWithdraw from '@/components/Deposit-Withdraw.vue';
import { reactive, onMounted } from 'vue';
import { getAllAccounts } from '@/methods/AccountMethods';
import { useAccountStore } from '@/stores/useAccountStore';
import { useRouter } from 'vue-router';

const router = useRouter()
const store = useAccountStore()

if (store.accountNumber.account_number === 9000) {
  router.push('/accounts')
}

const accounts = reactive({
  accountsList: [],
  isAccountsLoaded: false,
})

onMounted(async () => {
  const allAccounts = await getAllAccounts()
  accounts.accountsList = allAccounts.data
  accounts.isAccountsLoaded = true
})
</script>

<template>
  <section v-if="accounts.isAccountsLoaded" :class="['deposit-container']">
    <DepositWithdraw :title="'Deposit'" :type="'DEPOSIT'" :accounts="accounts.accountsList"  />
  </section>
</template>

<style lang="scss" scoped>
.deposit-container {
  height: 100vh;
  width: 100%;
  margin-left: 48px;
  padding: 1rem;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
