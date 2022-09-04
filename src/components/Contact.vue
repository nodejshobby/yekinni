<template>
   <section class="container-fluid section-padding" id="contact">
    <div class="row text-center section-header">
        <div class="col-12">
            <h2>Contact</h2>
            <p>Need to communicate with me on any projects or have anything to discussion with me</p>
        </div>
    </div>
    <div class="row justify-content-center align-items-center mt-2 px-5 g-4">
        <div class="col-11 col-md-10 col-lg-8 col-xl-6 mx-auto">
            <form action="https://formspree.io/f/mdojaapn" method="post">
                <div class="form-group mb-3">
                    <input class="form-control" type="text" name="subject" id="subject" placeholder="Subject" required>
                </div>
                <div class="form-group mb-3">
                    <input class="form-control" type="email" name="email" id="email" placeholder="Email" required>
                </div>
                <div class="form-group mb-3">
                    <input class="form-control" type="text" name="fullname" id="fullname" placeholder="Fullname" required>
                </div>
                <div class="form-group mb-3">
                    <textarea class="form-control" name="message" id="message" cols="30" rows="10" placeholder="Message" required></textarea>
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
    name: 'ContactSection'
}
</script>

<style>
    #contact {
        background-color: var(--primary-color);
        color: var(--secondary-color);
    }
    #contact-btn {
        padding: .8rem 3rem;
        background-color: var(--secondary-color);
        border-color: var(--dark-blue);
        color: var(--dark-blue);
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