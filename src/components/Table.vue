<script>
export default {
    data() {

        return {

            teams: [
                {
                    number: 1,
                    logo: '/src/assets/club-1.png',
                    name: 'Istanbul Sports',
                    victories: 18,
                    ties: 2,
                    lost: 0,
                    points: 42
                },
                {
                    number: 2,
                    logo: '/src/assets/club-2.png',
                    name: 'United Fs Club',
                    victories: 14,
                    ties: 2,
                    lost: 1,
                    points: 35
                },
                {
                    number: 3,
                    logo: '/src/assets/club-3.png',
                    name: 'Shalke Club',
                    victories: 13,
                    ties: 3,
                    lost: 0,
                    points: 32
                },
                {
                    number: 4,
                    logo: '/src/assets/club-4.png',
                    name: 'Inter Club',
                    victories: 13,
                    ties: 2,
                    lost: 1,
                    points: 31
                },
                {
                    number: 5,
                    logo: '/src/assets/league-club-5.png',
                    name: 'Madrid Club',
                    victories: 12,
                    ties: 1,
                    lost: 2,
                    points: 30
                },
                {
                    number: 6,
                    logo: '/src/assets/club-6.png',
                    name: 'Schalke Club',
                    victories: 11,
                    ties: 0,
                    lost: 3,
                    points: 28
                },
                {
                    number: 7,
                    logo: '/src/assets/club-7.png',
                    name: 'Arsenal Club',
                    victories: 10,
                    ties: 5,
                    lost: 0,
                    points: 26
                },
                {
                    number: 8,
                    logo: '/src/assets/club-8.png',
                    name: 'Bayern Club',
                    victories: 10,
                    ties: 2,
                    lost: 2,
                    points: 24
                },
                {
                    number: 9,
                    logo: '/src/assets/club-9.png',
                    name: 'Atletico Club',
                    victories: 9,
                    ties: 0,
                    lost: 4,
                    points: 20
                },
            ],

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
            ]
        };
    }
};
</script>


<template>

    <div id="container">
        <div class="tables">
            <h3>League Table</h3>
            <div class="tables-cnt">
                <div class="container-cards">
                    <table>
                        <thead>
                            <tr class="heading">
                                <th class="start">TEAM</th>
                                <th>W</th>
                                <th>D</th>
                                <th>L</th>
                                <th class="pts">PTS</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="team in teams">
                                <td>
                                    <div class="team-info">
                                        <span class="team-number">{{ team.number }}</span>
                                        <img :src="team.logo" alt="Logo Team">
                                        <span class="team-name">{{ team.name }}</span>
                                    </div>
                                </td>
                                <td>{{ team.victories }}</td>
                                <td>{{ team.ties }}</td>
                                <td>{{ team.lost }}</td>
                                <td class="pts">{{ team.points }}</td>
                            </tr>
                        </tbody>
                    </table>
                    <div class="final-btn">
                        View Full League Table
                    </div>
                </div>
            </div>
        </div>

        <div class="tables">
            <h3>Fixtures & Results</h3>
            <div class="tables-cnt">
                <div id="table-matches">
                    <div v-for="(match, index) in matches" :class="['match', (index % 2 === 0) ? 'first' : 'second']">
                        <div class="first-team">
                            <img :src="match.firstTeam.logo" alt="Team 1 Logo">
                            <span>{{ match.firstTeam.club }}</span>
                        </div>
                        <div class="vs">VS</div>
                        <div class="second-team">
                            <img :src="match.secondTeam.logo" alt="Team 2 Logo">
                            <span>{{ match.secondTeam.club }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="final-btn">
                View Full Fixtures
            </div>
        </div>
    </div>

    <div id="ads"></div>

</template>


<style lang="scss" scoped>

#container {
    width: 100%;
    background-color: #ffffff;
    padding: 40px;
    display: flex;
    justify-content: space-around;
}

#table-matches {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;

    img {
        width: 80px;
    }
}

h3 {
    color: black;
    font-size: 1.4em;
    margin-bottom: 20px;
}

.container-cards {
    margin: 20px auto;
    color: black;
    border-radius: 8px;
}

.match {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    gap: 180px;
    position: relative;
}

.first-team, .second-team {
    display: flex;
    align-items: center;
    color: black;
    font-size: 1.2em;
}

.second-team {
    flex-direction: row-reverse;
}

.vs {
    font-size: 1.4em;
    font-weight: bold;
    color: black;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}

.final-btn {
    height: 90px;
    background-color: black;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    font-size: 1.2em;
    cursor: pointer;
}

.tables {
    width: 42%;
    text-align: center;
}

.tables-cnt {
    width: 100%;
}

.first {
    background-color: #f3f3f3;
}

.second {
    background-color: #ebebeb;
}

table {
    width: 100%;
    border-collapse: collapse;
    font-size: 1.2em;
}

th, td {
    padding: 10px;
    text-align: center;
    border-bottom: 1px solid white;

    img {
        width: 56px;
    }
}

tbody {
    background-color: #f5f5f5;
}

thead {
    background-color: #212121;
    color: white;
}

.heading {
    font-size: 1.6em;
    font-weight: bold;
}

.pts {
    font-weight: bold;
}

.start {
    text-align: start;
}

.team-info {
    display: flex;
    align-items: center;
    gap: 20px;
}


#ads {
    width: 100%;
    height: 240px;
    background-image: url(/src/assets/reklam.jpg);
    background-size: cover;
    background-position: center;
}

</style>