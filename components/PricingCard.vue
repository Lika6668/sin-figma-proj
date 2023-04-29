<template>
 <div class="card" :class="{['card-' + data.color]: true }">
    <h3>{{ data.title }}</h3>
   <br>
   <h2>{{ data.price }}</h2>
   <span>{{ data.time }}</span>
   <br>
   <br>
   <ul>
    <li v-for="element, index in data.features" :key="index">{{ element }}</li>
   </ul>
   <div class="p-button">
        <v-btn class="button" elevation="4" size="x-large"
        :ripple="false"
        height="48">
        Choose Started
        </v-btn>
    </div>
 </div>
</template>
<script>
export default {
    props: ['data'],
}
</script>

<style scoped>
.card {
    text-align: center;
    border: 1px solid #D6D6D6;
    border-top-width: 0;
    border-radius: 0 0 6px 6px;
    padding: 22px 40px;
    line-height: 1.5;
    color: #6A6A6A;
    position: relative;
}

.card::before {
    content: '';
    position: absolute;
    top: -8px;
    left: -1px;
    right: -1px;
    height: 8px;
    border-radius: 6px 6px 0 0;
}

.card-gray::before {
    background: #d6d6d6;
}

.card-green::before {
    background: #0fa958;
}

.card-blue::before {
    background: #5551ff;
}

.card-orange::before {
    background: rgb(242, 78, 30);
}

.card-violet::before {
    background: rgb(162, 89, 255);
}
ul {
    list-style: none;
    margin: 0px;
    padding: 0px;
    text-align: left;
}
li {
    margin-bottom: 8px;
    background: url(data:image/svg+xml;base64,PHN2ZwogIHdpZHRoPSIyOSIKICBoZWlnaHQ9IjIxIgogIGZpbGw9Im5vbmUiCiAgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIgogIHZpZXdCb3g9IjAgMCAyOSAyMSIKPgogIDxwYXRoIHN0cm9rZT0iIzZBNkE2QSIgZD0iTTIgOS4zbDguOCA4LjdMMjcgMiIgc3Ryb2tlLXdpZHRoPSI0IiAvPgo8L3N2Zz4K) left 8px / 12px no-repeat;
    padding-left: 24px;
}
.p-button {
    padding: 50px;
}

.button {
    display: flex;
    flex-direction: column;
    position: absolute;
    left: 32px;
    right: 32px;
    bottom: 24px;
    cursor: pointer;
    color: #6A6A6A;
}
</style>