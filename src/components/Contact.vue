<template>
   <section class="container-fluid section-padding" id="contact">
    <div class="row text-center section-header">
        <div class="col-12">
            <h2>Contact</h2>
            <p>Need to communicate with me on any projects or have anything to discussion with me</p>
        </div>
    </div>
    <div class="row justify-content-center align-items-center mt-2 g-4">
        <div class="col-11 col-md-10 col-lg-8 col-xl-6 animate__animated animate__flipInX">
            <form action="https://formspree.io/f/mdojaapn" method="post" id="contactForm" @submit.prevent="handleSubmit">
                <div class="alert alert-success mb-3" v-if="success">
                    {{ success }}
                </div>
                <div class="alert alert-danger mb-3" v-if="error">
                    {{ error }}
                </div>
                <div class="form-group mb-3">
                    <input v-model.trim="subject" class="form-control" type="text" name="subject"  placeholder="Subject" required>
                </div>
                <div class="form-group mb-3">
                    <input v-model.trim="email" class="form-control" type="email" name="email"  placeholder="Email" required>
                </div>
                <div class="form-group mb-3">
                    <input v-model.trim="fullname" class="form-control" type="text" name="fullname"  placeholder="Fullname" required>
                </div>
                <div class="form-group mb-3">
                    <textarea v-model.trim="message" class="form-control" name="message"  cols="30" rows="10" placeholder="Message" required></textarea>
                </div>
                <div class="form-group mt-4 text-center">
                    <button class="btn btn-primary shadow" type="submit" id="contact-btn">Send</button>
                </div>
            </form>
        </div>
    </div>
    </section>
</template>

<script>
export default {
    name: 'ContactSection',
    data(){
        return {
            subject: '',
            email: '',
            fullname: '',
            message: '',
            error: null,
            success: null
        }
    },
    methods: {
        handleSubmit(e){
            var contactBtn=document.getElementById('contact-btn');
            contactBtn.innerText = "Processing...";
            var data = new FormData();
            data.append('subject', this.subject)
            data.append('email', this.email)
            data.append('fullname', this.fullname)
            data.append('message', this.message)

            fetch(e.target.action, {
                method: e.target.method,
                body: data,
                headers: {
                    'Accept': 'application/json'
                }
        }).then(response => {
            if(response.ok){
                this.success ="Thanks for your submission!";
            }else{
                this.error = "Oops! There was a problem submitting your form"
            }
            contactBtn.innerText = "Send";
            this.resetForm();
        }).catch(() => {
            this.error = "Oops! There was a problem submitting your form"
            contactBtn.innerText = "Send";
            this.resetForm();
        });
        },
        resetForm(){
            this.subject = ''
            this.fullname = ''
            this.email = ''
            this.message = ''
        }   
    }
}
</script>

<style>
    #contact {
        background-color: var(--primary-color);
        color: var(--secondary-color);
    }
    #contact-btn {
        padding: .8rem 3rem;
        background-color: var(--dark-blue);
        border-color: var(--dark-blue);
        color: var(--secondary-color);
        font-weight: 600;
        transition: all .5s ease;
    }

    input.form-control {
        height: 3.5rem;
        margin-bottom: 1rem;
    }
    textarea {
        resize: none;
    }
</style>