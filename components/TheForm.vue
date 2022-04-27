<template>
    <v-container
    id="contact"
    fluid
    class="bg-form"
    >
        <v-card
        class="mx-auto rounded-0"
        style="max-width: 500px;">
            <v-card-title class="card-title d-flex justify-center">Entre em Contato</v-card-title>
            <v-card-text class="d-flex justify-center my-n2">para conhecer muito mais do mundo dos gatos</v-card-text>
            <form
            class="pa-4 pt-6"
            >
                <v-text-field
                v-model="firstname"
                :error-messages="firstNameErrors"
                :counter="20"
                label="Primeiro Nome"
                required
                @input="$v.firstname.$touch()"
                @blur="$v.firstname.$touch()"
                ></v-text-field>
                <v-text-field
                v-model="lastname"
                :error-messages="lastNameErrors"
                :counter="20"
                label="Sobrenome"
                required
                @input="$v.lastname.$touch()"
                @blur="$v.lastname.$touch()"
                ></v-text-field>
                <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="E-mail"
                required
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"
                ></v-text-field>
                <v-text-field
                v-model="phoneNumber"
                v-mask="'(##) #####-####'"
                :error-messages="phoneErrors"
                label="Celular"
                required
                @input="$v.phoneNumber.$touch()"
                @blur="$v.phoneNumber.$touch()"
                ></v-text-field>
                <v-checkbox
                v-model="checkbox"
                title="Autorizar envio de dados"
                color="purple accent-2"
                :error-messages="checkboxErrors"
                label="Você autoriza o envio das informações?"
                required
                @change="$v.checkbox.$touch()"
                @blur="$v.checkbox.$touch()"
                ></v-checkbox>
                <button
                title="Enviar seus dados"
                class="mr-4 btn-form"
                @click="submit"
                >
                Enviar
                </button>
                <button
                title="Limpar seus dados"
                class="btn-form"
                @click="clear">
                Limpar
                </button>
            </form>
        </v-card>
    </v-container>
</template>

<script>
import { validationMixin } from 'vuelidate'
import { required, maxLength, email } from 'vuelidate/lib/validators'

export default {
    name: 'TheForm',
    mixins: [validationMixin],

    validations: {
        firstname: { required, maxLength: maxLength(20) },
        lastname: { required, maxLength: maxLength(20) },
        email: { required, email },
        phoneNumber: { required, maxLength: maxLength(15) },
        checkbox: {
            checked (val) {
            return val
            },
        },
    },

    data: () => ({
        firstname: '',
        lastname: '',
        email: '',
        phoneNumber: '',
        checkbox: false,
    }),

    computed: {
        checkboxErrors () {
            const errors = []
            if (!this.$v.checkbox.$dirty) return errors
            !this.$v.checkbox.checked && errors.push('Você deve concordar em enviar!')
            return errors
        },
        firstNameErrors () {
            const errors = []
            if (!this.$v.firstname.$dirty) return errors
            !this.$v.firstname.maxLength && errors.push('O nome deve ter no máximo 10 caracteres')
            !this.$v.firstname.required && errors.push('O nome é obrigatório.')
            return errors
        },
        lastNameErrors () {
            const errors = []
            if (!this.$v.lastname.$dirty) return errors
            !this.$v.lastname.maxLength && errors.push('O sobrenome deve ter no máximo 10 caracteres')
            !this.$v.lastname.required && errors.push('Sobrenome é obrigatório.')
            return errors
        },
        emailErrors () {
            const errors = []
            if (!this.$v.email.$dirty) return errors
            !this.$v.email.email && errors.push('Deve ser um e-mail válido')
            !this.$v.email.required && errors.push('Email é obrigatório.')
            return errors
        },
        phoneErrors() {
            const errors = []
            if (!this.$v.phoneNumber.$dirty) return errors
            !this.$v.phoneNumber.required && errors.push('Telefone é obrigatório.')
            return errors
        }
    },

    methods: {
        submit () {
            this.$v.$touch()
        },
        clear () {
            this.$v.$reset()
            this.firstname = ''
            this.lastname = ''
            this.email = ''
            this.phoneNumber = ''
            this.checkbox = false
        },
    },
}
</script>

<style scoped>
.bg-form {
    background: no-repeat center url( "/two-cat-heart.png");
    background-size: contain;
}

.card-title {
    color: #b48bcc;
}

.btn-form {
    background: #b48bcc;
    color: #fff;
    height: 45px;
    min-width: 64px;
    padding: 10px 25px;
    font-size: 16px;
    transition: all 0.2s;
}
.btn-form:hover {
    background: #e06cb9;
    box-shadow: 0 6px 12px #5e6697;
    transform: scale(1.1);
    position: relative;
    z-index: 1;
}
</style>