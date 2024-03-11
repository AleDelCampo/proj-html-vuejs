<script>

export default {
    data() {
        return {
            links: [ 
                "HOME",
                "FIXTURES & RESULTS",
                "LEAGUE TABLE",
                "PLAYERS",
                "GALLERY",
                "BLOG",
                "CONTACTS"
            ],
        };
    },
}
</script>


<template>

  <nav>

    <div id="navbar">

        <div id="labels-icons">

            <div>
                <img src="/src/assets/sponsor1.png" alt="Coca-Cola-Logo">
            </div>

            <div>
                <img src="/src/assets/sponsor2.png" alt="Nike-Logo">
            </div>

            <div>
                <img src="/src/assets/logo-football.png" alt="Football-Logo">
            </div>

            <div id="socials">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-twitter"></i>
            </div>
        </div>

        <div id="links">
            <div id="links-cnt">
                <div id="navbar-list">
                    <div>
                        <ul>
                            <li v-for="currentLink in links">
                                {{ currentLink }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <div id="title-container">
            <div  id="title-cnt">
                <h1>
                    Foot-Bool Club <br> Sport Club
                </h1>

                <span id="private-club">
                    Private Foot-Bool Matches
                </span>
                    <br>
                <button id="learn-more">
                    Learn More <i class="fa-solid fa-arrow-right"></i>
                </button>
            </div>
        </div>
    </div>

  </nav>

</template>


<style lang="scss" scoped>

#navbar {
    position: absolute;
    width: 100%;
    height: 30%;
    z-index: 2;
    background-color: rgba(0, 0, 0, 0.6);
    padding: 24px;
}

#labels-icons {
    
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 48px;

    img {
        cursor: pointer;
        transition: transform 0.4s ease;
    }

    img:hover {
        transform: scale(1.4);
    }
}

#socials {

    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-left: 12px;

    i {
        font-size: 40px;
        cursor: pointer;
        transition: transform 0.4s ease;
    }

    i:first-child {
        font-size: 36px;
    }

    i:hover {
        transform: scale(1.4);
    }
}

#links-cnt ul {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    gap: 60px; 
    list-style-type: none; 
    padding: 0;

    li {
        cursor: pointer;
        font-weight: bold;
        text-transform: uppercase;
        font-size: 1.2em;
        border-bottom: transparent 2px solid;
    }

    li:hover {
        border-bottom: white 2px solid;
    }
}

#title-container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 80px;
}

#title-cnt {
    width: 720px;
    height: 460px;
    text-align: center;
}

h1 {
    font-size: 80px;
    text-align: center;
}

#private-club, #learn-more {
    font-size: 1.2em;
    font-weight: bold;
}

#learn-more {
    margin-top: 40px;
    padding: 24px 48px;
    background-color: transparent;
    border: 2px white solid;
    border-radius: 24px;
    cursor: pointer;     
}

button {
    transition: transform 0.4s ease;
}

button:hover {
    transform: scale(1.2);
}

</style>