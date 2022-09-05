<template>
    <footer class="container-fluid" id="footer">
        <div class="row justify-content-center align-items-center">
            <div class="col-11 text-white text-center py-2 pt-4">
               <p>Copyright &copy; {{ new Date().getFullYear() }}. Built and Designed By <span class="highlighted"> Yekinni Basiru</span> </p> 
            </div>
        </div>
        <button class="btn btn-primary" @click="scrollTop" id="scrollTop"><i class="fa fa-arrow-up"></i></button>
    </footer>
</template>

<script>
export default {
    name: 'FooterSection',
    mounted(){
        this.scrollFunction();
    },
    methods: {
        scrollFunction(){
            var scrollbutton = document.getElementById("scrollTop");

            window.onscroll = function() { scrollFunction() };

            function scrollFunction() {
                if (document.body.scrollTop > 30 || document.documentElement.scrollTop > 30) {
                    scrollbutton.style.display = "block";
                } else {
                    scrollbutton.style.display = "none";
                }
            }
        },
        scrollTop(){
            document.body.scrollTop = 0; 
            document.documentElement.scrollTop = 0; 
        }
    }
}
</script>

<style>
    #footer {
        background-color: var(--dark-blue);
        position: absolute;
    }

    #footer p {
        font-size: .9rem;
    }

    .highlighted {
        color: var(--light-blue);
        font-weight: 600;
    }

    #scrollTop {
        position: fixed;
        display: none;
        right: 1rem;
        bottom: 1rem;
        cursor: pointer;
        z-index: 99;
        padding: .8rem 1rem;
        border: none;
        outline: none;
        border-radius: 10px;
        background-color: var(--light-blue);
    }

    #scrollTop i {
        font-size: 1.3rem;
    }
</style>
