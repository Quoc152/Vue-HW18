<script setup>
import CustomButton from "./components/CustomButton.vue";
import { UserIcon, ArrowRightIcon, MailIcon, SendIcon } from "lucide-vue-next";
</script>

<template>
  <div
    class="container h-screen py-8 flex flex-col gap-3 justify-center items-center"
  >
    <CustomButton>Demo Button</CustomButton>

    <CustomButton
      ><template #prefix-icon>
        <UserIcon class="h-5 w-5" />
      </template>
      With Prefix Icon
    </CustomButton>

    <CustomButton>
      With Suffix Icon
      <template #suffix-icon>
        <ArrowRightIcon class="h-5 w-5" />
      </template>
    </CustomButton>

    <CustomButton>
      <template #prefix-icon>
        <MailIcon class="h-5 w-5" />
      </template>
      With Both Icons
      <template #suffix-icon>
        <SendIcon class="h-5 w-5" />
      </template>
    </CustomButton>

    <CustomButton :isLoading="true"> Loading Button </CustomButton>
  </div>
</template>
