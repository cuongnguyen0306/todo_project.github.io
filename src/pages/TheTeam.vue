<template>
    <div>
        <h1 class="grey--text mb-3">Teams</h1>
        <v-layout row wrap>
            <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.id">
                <v-card class="ma-4">
                    <div class="d-flex justify-center pt-4 pb-2">
                        <v-avatar size="100">
                            <img :src="image">
                        </v-avatar>
                    </div>
                    <div class="d-flex justify-center">
                        <v-card-title class="pa-0">{{ person.name }}</v-card-title>
                    </div>
                    <v-card-subtitle class="text-center pa-0">{{ person.role }}</v-card-subtitle>
                    <v-card-actions class="d-flex justify-center pb-3">
                        <v-btn depressed>
                            <v-icon left>mdi-message</v-icon>
                            <span>Message</span>
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
import image from "@/assets/logo.png";
export default {
    data() {
        return {
            image,
            team: [
                { id: 1, name : 'Test', role: 'Team Lead', avatar: ''},
                { id: 2, name : 'DEMO', role: 'Frontend Developer', avatar: ''},
                { id: 3, name : 'API', role: 'Backend Developer', avatar: ''},
                { id: 4, name : 'VUEJS', role: 'Frontednd Developer', avatar: ''},
                { id: 5, name : 'DATA', role: 'Database Admin', avatar: ''},
                { id: 6, name : 'CƯỜNG NGUYỄN', role: 'Full Stack Developer', avatar: ''},
                { id: 7, name : 'CƯỜNG NGUYỄN', role: 'Full Stack Developer', avatar: ''},
            ]
        }
    }
}
</script>