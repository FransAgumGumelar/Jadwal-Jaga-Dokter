<template>
    <!-- sidebar 1 -->
    <v-navigation-drawer :width="60" theme="dark" permanent>
            <v-list-item value="dashboard" to="/" size="x-large">
                
            </v-list-item>

        <v-divider></v-divider>
            
            <v-list density="compact" nav>
                <v-list-item prepend-icon="mdi-shield-account-outline" value="dashboard" to="/"></v-list-item>
                <v-list-item prepend-icon="mdi-fishbowl-outline" value="messages" to=""></v-list-item>
                <v-list-item prepend-icon="mdi-fruit-grapes-outline" value="messages" to=""></v-list-item>
            </v-list>
        </v-navigation-drawer>
</template>