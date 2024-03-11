<script>
export default {
    data() {
    return {
      matches: [
        {
          firstTeam: { club: "Schalke Club", logo: "/src/assets/club-3.png" },
          secondTeam: { club: "Inter Club", logo: "/src/assets/club-4.png" }
        },
        {
          firstTeam: { club: "Atletic Club", logo: "/src/assets/club-9.png" },
          secondTeam: { club: "Schalke Club", logo: "/src/assets/club-6.png" }
        },
        {
          firstTeam: { club: "United Fs Club", logo: "/src/assets/club-2.png" },
          secondTeam: { club: "Bayern Club", logo: "/src/assets/club-8.png" }
        },
        {
          firstTeam: { club: "Arsenal Club", logo: "/src/assets/club-7.png" },
          secondTeam: { club: "Atletico Club", logo: "/src/assets/club-9.png" }
        },
        {
          firstTeam: { club: "Istanbul Sports", logo: "/src/assets/club-1.png" },
          secondTeam: { club: "United Fs Club", logo: "/src/assets/club-2.png" }
        }
      ],
      
      additionalData: [
        { date: `October 12, 2024 20:30 pm`, stadium: `Expert Stadium` },
        { date: `November 13, 2024 19:30 pm`, stadium: `Expert Stadium` },
        { date: `December 14, 2024 18:00 pm`, stadium: `Expert Stadium` },
        { date: `January 15, 2025 20:30 pm`, stadium: `Expert Stadium` },
        { date: `February 16, 2025 19:30 pm`, stadium: `Expert Stadium` },
      ]
    };
  }
};
</script>


<template>
    <div id="upcoming-matches">
        <h2>Upcoming Matches</h2>
        <div v-for="(match, index) in matches" class="match">
            <div class="first-team">
                <img :src="match.firstTeam.logo" alt="Team 1 Logo">
                <span>{{ match.firstTeam.club }}</span>
            </div>
            <div class="vs">VS</div>
            <div class="second-team">
                <img :src="match.secondTeam.logo" alt="Team 2 Logo">
                <span>{{ match.secondTeam.club }}</span>
            </div>
            <div class="additional-info">
                <div><i class="fa-solid fa-calendar-days"></i>{{ additionalData[index].date }}</div>
                <div><i class="fa-solid fa-circle-plus"></i>{{ additionalData[index].stadium }}</div>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>

#upcoming-matches {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  background-image: url('/src/assets/saha.jpg');
  background-size: cover;
  background-position: center;
}

h2 {
   padding: 20px;
}

.match {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
  width: 80%;
  height: 200px;
  background-color: rgba(0, 0, 0, 0.2);
  gap: 40px;
  position: relative;

  i {
    font-size: 14px;
    margin-right: 6px;
  }
}

.first-team, .second-team {
    display: flex;
    align-items: center;
    font-size: 1.4em;
    font-weight: bold;
}

.second-team {
  flex-direction: row-reverse;
}

.vs {
  font-size: 40px;
  font-weight: bold;
  margin: 0 10px;
}

.additional-info {
    display: flex;
    justify-content: center;
    position: absolute;
    gap: 30px;
    bottom: 0;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.4);
    font-weight: bold;
}

</style>