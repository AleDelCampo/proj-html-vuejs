<script>
</script>


<template>

    <div id="footer-container">
        <div id="footer-cnt">
            <div id="ref-container">
                <img src="/src/assets/logo-footer-football.png" alt="Logo Team">
                <span class="references"><i class="fa-solid fa-location-dot icon"></i> New Jersey, USA</span>
                <span class="references"><i class="fa-solid fa-phone-volume icon"></i>+1 (234) 567 89 10</span>
                <span class="references"><i class="fa-regular fa-envelope icon"></i>alehashirama@gmail.com</span>
                <div id="icon-cnt">
                    <div class="social-icon">
                        <i class="fa-brands fa-facebook-f"></i>
                    </div>
                    <div class="social-icon">
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                    <div class="social-icon">
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                </div>
            </div>

            <div>
                <h4>Join Our Newsletter</h4>
                <p>Subscribe to be informed about important developments <br>    in our club and football world.</p>
                <div>
                    <input class="newsletters" type="email" placeholder="Enter Your Email Here....">
                </div>
                <div>
                    <button class="newsletters">
                        Subscribe Newsletter<i class="fa-solid fa-arrow-right"></i>
                    </button>
                </div>
            </div>

            <div>
                <ul>
                    <h4>Education</h4>
                    <li><i class="fa-solid fa-minus"></i>FIXTURES & RESULTS</li>
                    <li><i class="fa-solid fa-minus"></i>LEAGUE TABLE</li>
                    <li><i class="fa-solid fa-minus"></i>PLAYERS</li>
                    <li><i class="fa-solid fa-minus"></i>GALLERY</li>
                </ul>
            </div>

            <div>
                <ul>
                    <h4>Quick Links</h4>
                    <li><i class="fa-solid fa-minus"></i>HOME</li>
                    <li><i class="fa-solid fa-minus"></i>BLOG</li>
                    <li><i class="fa-solid fa-minus"></i>GALLERY</li>
                    <li><i class="fa-solid fa-minus"></i>CONTACT</li>
                </ul>
            </div>
        </div>
        <div id="copyright">
            © 2024 Foot-Bool Club - All Rights Reserved.
        </div>
    </div>

</template>


<style lang="scss" scoped>
#footer-container {
    width: 100%;
    height: 460px;
    background-image: url(/src/assets/footer-bg-football.jpg);

    img {
        width: 80px;
        margin-bottom: 20px;
        cursor: pointer;
    }
}

#footer-cnt {
    display: flex;
    justify-content: space-between;
    padding: 40px;
}

#copyright {
    width: 100%;
    text-align: center;
}

#ref-container {
    display: flex;
    flex-direction: column;
}

#icon-cnt {
    display: flex;
    gap: 40px;
}

.icon {
    font-size: 28px;
    margin-right: 20px;
    margin-bottom: 20px;
    cursor: pointer;
}

.social-icon {
    font-size: 36px;
    padding: 4px 40px;
    border: 1px solid white;
}

.social-icon:hover {
    cursor: pointer;
    transform: scale(1.4);
}

h4 {
    margin-bottom: 20px;
    font-size: 1.8em;
}

ul {
    display: flex;
    flex-direction: column;
    list-style-type: none;

    i {
        font-size: 24px;
    }
}

ul li {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 12px;
}

li:hover {
    cursor: pointer;
}

p {
    margin-bottom: 20px;
}

input {
    width: 400px;
    height: 80px;
    margin-bottom: 12px;
    background-color: white;    
}

.newsletters {
    width: 400px;
    height: 80px;
    border-radius: 24px;
    background-color: white;
    color: black;
    font-size: 1.2em;
    cursor: pointer;
}
</style>