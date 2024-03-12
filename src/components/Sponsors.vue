<script>
export default {

    data() {

        return {

            sponsors: [
                {
                    sponsorImg: '/src/assets/client2.png',
                },
                {
                    sponsorImg: '/src/assets/client3.png',
                },
                {
                    sponsorImg: '/src/assets/client4.png',
                },
                {
                    sponsorImg: '/src/assets/client7.png',
                },
                {
                    sponsorImg: '/src/assets/client9.png',
                },
                {
                    sponsorImg: '/src/assets/client10.png',
                }
            ]
        };
    }
}
</script>


<template>

    <div id="sponsor-container">

        <div id="sponsor-cards">
 
            <div v-for="card in sponsors" class="card">
                <img :src="card.sponsorImg">
            </div>

        </div>

    </div>

</template>


<style lang="scss">
#sponsor-container {
    width: 100%;
    background-color: black;
    display: flex;
    justify-content: center;
}

#sponsor-cards {
    display: flex;
    padding: 60px;
    gap: 60px;
    align-items: center;
}

.card {
    border: 1px white solid;
    border-radius: 24px;
    padding: 12px;
    cursor: pointer;
}
</style>