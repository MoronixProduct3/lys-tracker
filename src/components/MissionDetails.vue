<template>
    <v-row dense>
        <v-col cols="12" md="6" lg="3">
            <Map :m=missionObject.deployement></Map>
        </v-col>
        <v-col cols="12" md="6" lg="3">
            <Rule :r=missionObject.rule></Rule>
        </v-col>
        <v-col cols="12" md="6" lg="3">
            <Rule :r=missionObject.primary></Rule>
        </v-col>
        <v-col cols="12" md="6" lg="3">
            <Map :m=missionObject.map></Map>
        </v-col>
    </v-row>
</template>

<script setup>
import { computed, ref } from 'vue'

const dep = {
    crucible: {
        image: "PN_CrucibleOfBattle.webp",
        name: "CRUCIBLE OF BATTLE"
    },
    dawn: {
        image: "PN_DawnOfWar.webp",
        name: "DAWN OF WAR"
    },
    hammer: {
        image: "PN_HammerAndAnvil.webp",
        name: "HAMMER AND ANVIL"
    },
    search: {
        image: "PN_SearchAndDestroy.webp",
        name: "SEARCH AND DESTROY"
    },
    sweeping: {
        image: "PN_SweepingEngagement.webp",
        name: "SWEEPING ENGAGEMENT"
    },
    tipping: {
        image: "PN_TippingPoint.webp",
        name: "TIPPING POINT"
    },
}

const maps = {
    1: {
        name: 'WTC 1: Search and Destroy - MEDIUM',
        image: 'WTC_map1.png'
    },
    7: {
        name: 'WTC 7: Hammer and Anvil - MEDIUM',
        image: 'WTC_map7.png'
    },
    9: {
        name: 'WTC 9: Search and Destroy - MEDIUM',
        image: 'WTC_map9.png'
    },
    51: {
        name: 'WTC 51: Tipping Point - MEDIUM',
        image: 'WTC_map51.png'
    },
    54: {
        name: 'WTC 54: Tipping Point - MEDIUM',
        image: 'WTC_map54.png'
    },
}

const mis = {
    smoke: {
        name: 'SMOKE AND MIRRORS',
        text: 'After both players have deployed their armies, starting with the Attacker, each player can place one unit from their army that is on the battlefield into Strategic Reserves, regardless of how many units are already in Strategic Reserves.<br>The points value of such a unit cannot exceed 25% of each player\'s total points limit for the chosen battle size(500pts).'
    },
    banners: {
        name: 'RAISE BANNERS',
        text: 'At the end of each player’s turn, if a BATTLELINE unit from their army is within range of an objective marker that player controls, that unit raises a banner on that objective marker: that player scores 1VP (which is counted towards their Secondary Mission score), and that player’s units can no longer raise a banner on that objective marker.'
    },
    fog: {
        name: 'FOG OF WAR',
        text: 'In the first battle round, units have the Benefit of Cover, and players cannot use Core Stratagems (excluding the New Orders Stratagem).'
    },
    hidden: {
        name: 'HIDDEND SUPPLIES',
        text: 'In the Place Objective Markers step, players must set up one additional objective marker in No Man’s Land.<br>\
            Before setting up this new objective marker, players must first move the objective marker in the centre of the battlefield 6" directly towards one of the corners of the battlefield (if No Man’s Land touches any of the corners of the battlefield, you must move the objective marker towards one of those corners). Otherwise, the players roll-off, and the winner selects which corner the objective marker is moved towards. Players then set up the new objective marker 6" from the centre of the battlefield towards the diagonally opposite corner of the battlefield to the previously moved objective marker.'
    }
}

const prim = {
    purge: {
        name: 'PURGE THE FOE',
        text: "<i>ANY BATTLE ROUND:</i><br>\
            WHEN: End of the battle round.<br>\
            Each player scores 4VP if one or more enemy units were destroyed this battle round.<br>\
            <i>SECOND BATTLE ROUND ONWARDS:</i><br>\
            WHEN: End of the battle round.<br>\
            Each player scores 4VP if more enemy units than friendly units were destroyed this battle round.<br>\
            WHEN: End of the Command phase (or the end of your turn if it is the fifth battle round and you are going second).<br>\
            The player whose turn it is scores 4VP if they control one or more objective markers, and an additional 4VP if they control more objective markers than their opponent controls."
    },
    linchpin: {
        name: 'LINCHPIN',
        text: "<i>SECOND BATTLE ROUND ONWARDS:</i><br>\
            WHEN: End of the Command phase (or the end of your turn if it is the fifth battle round and you are going second).<br>\
            If the player whose turn it is does not control the objective marker in their deployment zone, they score 3VP for each objective marker they control.<br>\
            OR<br>\
            If the player whose turn it is controls the objective marker in their deployment zone, they score 3VP for controlling that objective marker, and 5VP for each other objective marker they control."
    },
    take: {
        name: 'TAKE AND HOLD',
        text: '<i>SECOND BATTLE ROUND ONWARDS</i><br>\
            WHEN: End of the Command phase (or the end of your turn if it is the fifth battle round and you are going second).<br>\
            The player whose turn it is scores 5VP for each objective marker they control(up to 15VP per turn).'
    },
    drop: {
        name: 'SUPPLY DROP',
        text: 'Start of the Battle: Players randomly select two different objective markers in No Man’s Land; the first selected is the Alpha objective, the second selected is the Omega objective.<br>\
            Start of the Fourth Battle Round: The Alpha objective is removed from the battlefield.<br>\
            Start of the Fifth Battle Round: All objective markers in No Man’s Land apart from the Omega objective are removed from the battlefield.<br>\
            <i>SECOND BATTLE ROUND ONWARDS</i><br>\
            WHEN: End of the Command phase (or the end of your turn if it is the fifth battle round and you are going second).<br>\
            The player whose turn it is scores the following VP for each objective marker in No Man’s Land that they control, depending on the current battle round:\
            <ul>\
                <li>5VP in the second and third battle rounds.</li>\
                <li>8VP in the fourth battle round.</li>\
                <li>15VP in the fifth battle round.</li>'
    }
}

const gw_m = {
    j: {
        deployement: dep.search,
        primary: prim.linchpin,
        rule: mis.banners,
        map: maps[1]
    },
    b: {
        deployement: dep.tipping,
        primary: prim.purge,
        rule: mis.smoke,
        map: maps[51]
    },
    c: {
        deployement: dep.tipping,
        primary: prim.linchpin,
        rule: mis.fog,
        map: maps[54]
    },
    l: {
        deployement: dep.search,
        primary: prim.take,
        rule: mis.hidden,
        map: maps[9]
    },
    h: {
        deployement: dep.hammer,
        primary: prim.drop,
        rule: mis.fog,
        map: maps[7]
    }
}

const props = defineProps({
    missionIndex: {
        require: true
    }
})

const missionObject = computed(() => {
    return gw_m[props.missionIndex];
})

</script>