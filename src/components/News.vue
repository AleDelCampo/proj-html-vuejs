<script>

export default {
    data() {
        return {
            news: [
                { newsCard: { photo: "/src/assets/news1-1.png", label: "18/02/2024", title: "What Is Foot-Bool??", description: "Foot-Bool is a sport that is known as a ball game and is loved by [...]" } },
                { newsCard: { photo: "/src/assets/news3-1.png", label: "24/02/2024", title: "Foot-Bool Rules", description: "GOLDEN GOAL: In a Foot-Bool match, the goal scored by one of the teams in [...]" } },
                { newsCard: { photo: "/src/assets/news2-1.png", label: "28/02/2024", title: "Foot-Bool Features", description: "Foot-Bool: It is an aerobic-based anaerobic sport in which jumps, kicks, turns, running with changing [...]" } },
                { newsCard: { photo: "/src/assets/news4-1.png", label: "02/03/2024", title: "Foot-Bool Terms", description: "GOLDEN GOAL: In a Foot-Bool match, the goal scored by one of the teams in [...]" } },
                { newsCard: { photo: "/src/assets/news6-1.png", label: "04/03/2024", title: "Foot-Bool Stadium", description: "In the Foot-Bool match, everything is permitted, but only with sports [...]" } }
            ],
            itemsPerPage: 4,
            currentPage: 0
        };
    },

    computed: {

        pageCount() {
            return Math.ceil(this.news.length / this.itemsPerPage);
        },

        paginatedNews() {
            const startIndex = this.currentPage * this.itemsPerPage;
            const endIndex = startIndex + this.itemsPerPage;
            return this.news.slice(startIndex, endIndex);
        }
    },

    methods: {

        goToPage(pageNumber) {
            if (pageNumber >= 0 && pageNumber < this.pageCount) {
                this.currentPage = pageNumber;
                this.shuffleNews();
            }
        },

        shuffleNews() {
            /*Qui utilizzo l'Array di Fisher-Yates*/
            for (let i = this.news.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [this.news[i], this.news[j]] = [this.news[j], this.news[i]];
            }
        }
    }
};
</script>



<template>

    <div id="news-container">
        <div id="news-cnt">
            <div>
                <i class="fa-regular fa-thumbs-up"></i>
            </div>
            <span id="articles">Notizie e Articoli Recenti</span>
            <span>Rimani aggiornato sul mondo del Foot-Bool</span>

            <div id="news-cards">
                <div v-for="(item, index) in paginatedNews" :key="index" class="new-cards">
                    <img :src="item.newsCard.photo" alt="Foto Notizia">
                    <div class="news-info">
                        <span class="news-label">{{ item.newsCard.label }}</span>
                        <h2 class="news-title">{{ item.newsCard.title }}</h2>
                        <p class="news-description">{{ item.newsCard.description }}</p>
                    </div>
                    <button>
                        More
                    </button>
                </div>
            </div>

            <div class="pagination">
                <div class="page-bar" @click="goToPage(0)"></div>
                <div class="page-bar" @click="goToPage(0)"></div>
                <div class="page-bar" @click="goToPage(0)"></div>
                <div class="page-bar" @click="goToPage(0)"></div>
            </div>
        </div>
    </div>

</template>


<style lang="scss" scoped>

#news-container {
    width: 100%;
    height: 1200px;
    background-color: #fbfbfb;
    display: flex;
    justify-content: center;
    padding: 40px;
}

#news-cnt {
    display: flex;
    align-items: center;
    flex-direction: column;
    color: black;

    i {
        font-size: 60px;
    }

    #articles {
        font-size: 2em;
        font-weight: bold;
    }

    span:nth-child(3) {
        margin-bottom: 40px;
    }
}

#news-cards {
    display: flex;
    gap: 40px;
    width: 100%;
    margin-bottom: 240px;
}

.new-cards {
    width: 100%;
    text-align: center;
    padding: 40px 12px;
    border-radius: 24px;
    background-color: #ffffff;
}

button {
    margin-top: 20px;
    padding: 24px 48px;
    background-color: black;
    border: 2px black solid;
    border-radius: 24px;
    font-size: 1.2em;
    font-weight: bold;
    transition: transform 0.4s ease;
    cursor: pointer;
}

button:hover {
    transform: scale(1.2);
}

.pagination {
    display: flex;
    justify-content: center;
    gap: 10px;
}

.page-bar {
    width: 80px;
    height: 20px;
    background-color: #b9b9b9;
    border: 2px solid black;
    border-radius: 40px;
    cursor: pointer;
}

.page-bar:hover {
    background-color: black;
    width: 120px;
}
</style>