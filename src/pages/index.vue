<template>
  <div>
    <BannerInfo />
    <Services />
    <BannerAboutUs />
    <LastProjects />
    <WorkWithUs />
  </div>
</template>

<script>
import BannerInfo from "~/components/BannerInfo";
import Services from "~/components/Services";
import BannerAboutUs from "~/components/BannerAboutUs";
import LastProjects from "~/components/LastProjects";
import WorkWithUs from "~/components/WorkWithUs";

export default {
  name: "IndexPage",
  components: {
    BannerInfo,
    Services,
    BannerAboutUs,
    LastProjects,
    WorkWithUs,
  },
};
</script>
