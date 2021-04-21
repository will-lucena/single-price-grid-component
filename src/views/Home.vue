<template>
  <div class="content">
    <custom-header
      :title="headerTitle"
      :subTitle="headerSubTitle"
      :description="headerDescription"
    ></custom-header>
    <div class="product-section">
      <purcharse
        :title="purcharseTitle"
        :value="purcharseValue"
        :frequency="purcharseFrequency"
        :description="purcharseDescription"
      ></purcharse>
      <about :title="aboutTitle" :reasons="aboutReasons"></about>
    </div>
  </div>
</template>

<script>
import About from "../components/About.vue";
import CustomHeader from "../components/CustomHeader.vue";
import Purcharse from "../components/Purcharse.vue";
export default {
  components: { Purcharse, CustomHeader, About },
  data() {
    return {
      headerTitle: "Join our community",
      headerSubTitle: "30-day, hassle-free money back guarantee",
      headerDescription: `Gain access to our full library of tutorials along with expert code reviews. 
        Perfect for any developers who are serious about honing their skills.`,
      purcharseTitle: "Monthly Subscription",
      purcharseValue: 29,
      purcharseFrequency: "per month",
      purcharseDescription: "Full access for less than $1 a day",
      aboutTitle: "Why Us",
      aboutReasons: [
        "Tutorials by industry experts",
        "Peer & expert code review",
        "Coding exercises",
        "Access to our GitHub repos",
        "Community forum",
        "Flashcard decks",
        "New videos every week",
      ],
    };
  },
};
</script>

<style></style>
