<script>

export default {

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
            
        </div>

    </div>

  </nav>

</template>


<style lang="scss">

#labels-icons {

    position: fixed;
    width: 100%;
    height: 30%;
    z-index: 2;
    background-color: rgba(0, 0, 0, 0.6);
    display: flex;
    justify-content: center;
    align-items: center;

    img {
        cursor: pointer;
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
    }

    i:first-child {
        font-size: 36px;
    }
    
}

</style>
