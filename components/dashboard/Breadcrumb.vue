<script setup>
import { NuxtLink } from '#components'

defineProps({
  title: {
    type: String,
    required: true,
  },
})
const { title } = useAppConfig()
</script>

<template>
  <Breadcrumb class="flex justify-between">
    <BreadcrumbList>
      <BreadcrumbItem>
        <BreadcrumbLink
          :as="NuxtLink"
          to="/dashboard"
        >
          Dashboard
        </BreadcrumbLink>
      </BreadcrumbItem>
      <BreadcrumbSeparator />
      <BreadcrumbItem>
        <BreadcrumbPage>Redirects</BreadcrumbPage>
      </BreadcrumbItem>
    </BreadcrumbList>

    <DashboardLogout />
  </Breadcrumb>
</template>
