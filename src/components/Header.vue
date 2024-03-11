<script>
export default {  
};
</script>


<template>
    
  
    <div id="match-container">
        
        <div id="match-cnt">
        <span>Istanbul Sports</span>
        <img src="/src/assets/club-1.png" alt="Club 1">
        <span>VS</span>
        <img src="/src/assets/club-2.png" alt="Club 2">
        <span>United Fs Club</span>
        </div>

        <div id="match-time">

            <span>
                <i class="fa-solid fa-calendar-days"></i> March 13, 2024 18:04 pm
            </span>

            <span>
                <i class="fa-solid fa-circle-plus"></i> Expert Stadium
            </span>

        </div>

        <div>
            <button>
                View Match Details
            </button>
        </div>

    </div>

    
</template>


<style lang="scss" scoped>

#match-container {

    width: 100%;
    height: 400px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: black;
    background-color: #ffffff;

}

#match-cnt {
    
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 36px;

    span {
        font-size: 2em;
        font-weight: bold;
    }

    span:nth-child(3) {
        font-size: 4em;
    }
}

#match-time {
    display: flex;
    gap: 34px;
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

</style>