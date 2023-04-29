<template>
    <v-card class="section-card" shaped elevation="24">
        <v-card-text>
            <v-row class="block-card">
                <p class="text-card">Join other industry-leading organizations pushing boundaries and solving problems in Figma</p> 
            <div class="cards">
                <v-img width="64" src="https://cdn.sanity.io/images/599r6htc/localized/5cc4ec7efbf529d23d98eb5cea426716848fbd56-77x77.svg?q=75&fit=max&auto=format"></v-img>
                <v-img width="64" src="https://cdn.sanity.io/images/599r6htc/localized/ae44fb1f0119d84e2fdadaadf20c7c6f3cc57e76-78x77.svg?q=75&fit=max&auto=format"> </v-img>
                <v-img width="64" src="https://cdn.sanity.io/images/599r6htc/localized/17b5b66d29a94a2e06bec865e350c55563ac4b59-78x77.svg?q=75&fit=max&auto=format"> </v-img>
                <v-img width="64" src="https://cdn.sanity.io/images/599r6htc/localized/b0c4a3e058a3e978a66b86716cc5cf908a107139-78x77.svg?q=75&fit=max&auto=format"> </v-img>
                <v-img width="64" src="https://cdn.sanity.io/images/599r6htc/localized/5e7d9f4dc1a2ad8bb116a3bdf1ff010b6e3e895f-78x77.svg?q=75&fit=max&auto=format"></v-img>
            </div>
        </v-row>
    </v-card-text>
</v-card>

</template>

<style scoped>
.section-card {
    padding-top: 50px;
    padding-bottom: 95px;
    width: 100%;
}

.block-card {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-inline: auto;
    max-width: 80%;
    text-align: center;
}

.text-card {
    padding-top: 30px;
    margin-bottom: 64px;
    width: 60%;
    text-align: center;
    line-height: 1.8;
    color: black;
    font-size: 17px;
}
.cards {
    display: inline-flex;
    flex-wrap: wrap;
    gap: 72px 80px;
    place-items: center;
    margin: auto;
    cursor: pointer;
}

</style>