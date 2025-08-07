<template>
    <v-container class="d-flex justify-center">
        <v-card width="400">
            <v-card-title class="text-h5">ログイン</v-card-title>
            <v-card-text>
                <v-form @submit.prevent="login">
                    <v-text-field
                        v-model="email"
                        label="メールアドレス"
                        required
                    ></v-text-field>
                    <v-text-field
                        v-model="password"
                        label="パスワード"
                        type="password"
                        required
                    ></v-text-field>
                    <v-btn type="submit" color="primary" block>ログイン</v-btn>
                </v-form>
                <v-alert type="error" v-if="errorMessage" class="mt-3">
                    {{ errorMessage }}
                </v-alert>
            </v-card-text>
        </v-card>
    </v-container>
</template>

<script>
export default {
    name: "Login",
    data() {
        return {
            email: "",
            password: "",
            errorMessage: "",
        };
    },
    methods: {
        login() {
            console.log("ログインボタンがクリックされました");
        },
    },
};
</script>
