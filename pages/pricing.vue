<template>
  <v-container>
    <v-col align="center">
      <PricingSelect v-on:selectType="onSelectType"/>
    <div class="text-pricing">
      <h1>Pricing</h1>
    </div>
      <div class="cards-grid">
        <PricingCard v-bind:data="data[type][0]"/>
        <PricingCard v-bind:data="data[type][1]"/>
        <PricingCard v-bind:data="data[type][2]"/>
      </div>
    </v-col>
  </v-container>
</template>

<script>
import PricingCard from '~/components/PricingCard.vue';
import PricingSelect from '~/components/PricingSelect.vue';


export default {
    data() {
        return {
            type: 0,
            data: [
                [
                    {
                        title: "Starter",
                        price: "Free",
                        color: "gray",
                        time: "Forever",
                        features: [
                            "3 Figma and 3 FigJam files",
                            "Unlimited personal files",
                            "Unlimited collaborators",
                            "Plugins, widgets, and templates",
                            "Mobile app",
                        ],
                    },
                    {
                        title: "Starter",
                        price: "Free",
                        color: "green",
                        time: "Forever",
                        features: [
                            "Unlimited Figma files",
                            "Unlimited version history",
                            "Sharing permissions",
                            "Shared and private projects",
                            "Team libraries",
                            "Audio conversations",
                        ],
                    },
                    {
                        title: "Starter",
                        price: "Free",
                        color: "blue",
                        time: "Forever",
                        features: [
                            "Org-wide libraries",
                            "Design system analytics",
                            "Branching and merging",
                            "Centralized file management",
                            "Unified admin and billing",
                            "Private plugins and widgets",
                            "Single sign-on",
                        ],
                    },
                ],
                [
                    {
                        title: "Starter",
                        price: "Free",
                        color: "gray",
                        time: "Forever",
                        features: [
                            "3 Figma and 3 FigJam files",
                            "Unlimited personal files",
                            "Unlimited collaborators",
                            "Plugins, widgets, and templates",
                            "Mobile app",
                            "Music player",
                            "Ready-made templates",
                        ],
                    },
                    {
                        title: "Starter",
                        price: "Free",
                        color: "orange",
                        time: "Forever",
                        features: [
                            "Unlimited FigJam files",
                            "Open sessions",
                            "Sharing permissions",
                            "Team libraries",
                            "Audio conversations",
                            "Voting",
                        ],
                    },
                    {
                        title: "Starter",
                        price: "Free",
                        color: "violet",
                        time: "Forever",
                        features: [
                            "Org-wide libraries",
                            "Centralized file management",
                            "Unified admin and billing",
                            "Private plugins and widgets",
                            "Single sign-on",
                        ],
                    },
                ],
            ],
        };
    },
    methods: {
        onSelectType(type) {
            this.type = type;
        }
    },
    components: { PricingCard, PricingSelect }
}
</script>

 <style scoped>

 .text-pricing {
    margin-top: 70px;
 }

 h1 {
    font-size: 60px;
 }
 .cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
  margin: 80px auto 40px;
 }
</style>