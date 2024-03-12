<script>
export default {
    data() {
        return {
            players: [
                {
                    playerCard: { photo: "/src/assets/player1.jpg", number: "07", name: "Adam Brown", role: "Forwarder" },
                },
                {
                    playerCard: { photo: "/src/assets/player2.jpg", number: "09", name: "Michael Kayn", role: "Forwarder" },
                },
                {
                    playerCard: { photo: "/src/assets/player3.jpg", number: "11", name: "Michael Lee", role: "Forwarder" },
                },
                {
                    playerCard: { photo: "/src/assets/player4.jpg", number: "15", name: "Ethan Smith", role: "Midfielder" },
                },
            ],

            newPlayers: [
                {
                    playerCard: { photo: "/src/assets/player5.jpg", number: "23", name: "John Bool", role: "Defender" },
                },
                {
                    playerCard: { photo: "/src/assets/player6.jpg", number: "10", name: "Ean Rossi", role: "Goalkeeper" },
                },
            ],
            allPlayers: false
        };
    },
};
</script>


<template>

    <div id="cards-container">
        <h2>Players</h2>
        <div id="cards-cnt">
            <div v-for="player in players" class="card-player">
                <img :src="player.playerCard.photo" alt="Player Photo">
                <div class="card-description">
                    <span>{{ player.playerCard.number }}</span>
                    <br>
                    <span>{{ player.playerCard.name }} - </span>
                    <span>{{ player.playerCard.role }}</span>
                </div>
            </div>
        </div>
        <div v-if="allPlayers" id="new-cards-container">
            <div v-for="player in newPlayers" class="card-player">
                <img :src="player.playerCard.photo" alt="Player Photo">
                <div class="card-description">
                    <span>{{ player.playerCard.number }}</span>
                    <br>
                    <span>{{ player.playerCard.name }} - </span>
                    <span>{{ player.playerCard.role }}</span>
                </div>
            </div>
        </div>

        <div id="btn">
            <button @click="allPlayers = !allPlayers">
                View All Players
            </button>
        </div>
    </div>

</template>


<style lang="scss" scoped>

#cards-container {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    width: 100%;

    background-image: url('/src/assets/player.jpg');
    background-size: cover;
    background-position: center;
}

#cards-cnt {
    display: flex;
    gap: 60px;
}

.card-player {
    position: relative;

    img {
        border-radius: 24px;
    }
}

.card-description {
    border-radius: 24px;
    background-color: black;
    text-align: center;
    position: absolute;
    bottom: 0;
    width: 100%;
    padding: 10px;

    span {
        font-size: 1.2em;
    }

    span:first-child {
        font-weight: bold;
        font-size: 1.6em;
    }
}

#new-cards-container {
    margin-top: 40px;
    display: flex;
    gap: 60px;
}


h2 {
    font-size: 2em;
    padding: 60px;
}

#btn {
    padding: 60px;
}

button {
    margin-top: 20px;
    padding: 24px 48px;
    background-color: black;
    border: 2px white solid;
    border-radius: 24px;
    font-size: 1.2em;
    font-weight: bold;
    transition: transform 0.4s ease;
    cursor: pointer;
}

button:hover {
    transform: scale(1.2);
}
</style>