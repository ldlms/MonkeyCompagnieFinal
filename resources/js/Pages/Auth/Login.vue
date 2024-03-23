<script setup>
import Checkbox from '@/Components/Checkbox.vue';
import GuestLayout from '@/Layouts/GuestLayout.vue';
import InputError from '@/Components/InputError.vue';
import InputLabel from '@/Components/InputLabel.vue';
import PrimaryButton from '@/Components/PrimaryButton.vue';
import TextInput from '@/Components/TextInput.vue';
import { Head, Link, useForm } from '@inertiajs/vue3';

defineProps({
});

const form = useForm({
    email: '',
    password: '',
    remember: false,
});

const submit = () => {
    form.post(route('login'), {
        onFinish: () => form.reset('password'),
    });
};
</script>

<template>
        <form @submit.prevent="submit">
            <div>
                <InputLabel for="email" value="Email" />

                <TextInput
                    id="email"
                    type="email"
                    class="mt-1 block w-full"
                    v-model="form.email"
                    required
                    autofocus
                    autocomplete="username"
                />

                <InputError id="errorEmail" class="mt-2" :message="form.errors.email" />
            </div>

            <div class="mt-4">
                <InputLabel for="password" value="Password" />

                <TextInput
                    id="password"
                    type="password"
                    class="mt-1 block w-full"
                    v-model="form.password"
                    required
                    autocomplete="current-password"
                />

                <InputError id="errorPassword" class="mt-2" :message="form.errors.password" />
            </div>
            <div class="flex items-center justify-end mt-4">
                <PrimaryButton class="ml-4" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                    Log in
                </PrimaryButton>
            </div>
        </form>
</template>

<style scoped>
/* Reset des styles pour le formulaire */
form {
    margin: 0;
    padding: 0;
}

/* Style général pour les étiquettes de champ */
label {
    display: block;
    font-weight: bold;
    margin-bottom: 0.5rem;
    color: #333; /* Couleur du texte de l'étiquette */
}

/* Style pour les champs de saisie */
input {
    width: calc(100% - 1rem);
    padding: 0.75rem;
    margin-bottom: 1rem;
    box-sizing: border-box;
    border: 1px solid #ddd; /* Bordure grise */
    border-radius: 4px; /* Coins arrondis */
}

/* Style pour les messages d'erreur */
.error-message {
    color: red;
    margin-top: 0.5rem;
}

/* Style pour le bouton de soumission */
button {
    padding: 1rem;
    background-color: #4CAF50; /* Vert */
    color: #fff; /* Texte blanc */
    border: none;
    cursor: pointer;
    border-radius: 4px; /* Coins arrondis */
}

/* Style pour le bouton de soumission désactivé */
button[disabled] {
    background-color: #ccc;
    cursor: not-allowed;
}
</style>
