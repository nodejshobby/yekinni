<template>
    <footer class="container-fluid" id="footer">
        <div class="row justify-content-center align-items-center">
            <div class="col-11 text-white text-center py-2 pt-4">
               <p>Copyright &copy; {{ new Date().getFullYear() }}. Built and Designed By <span class="highlighted"> Yekinni Basiru</span> </p> 
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterSection'
}
</script>

<style>
    #footer {
        background-color: var(--dark-blue);
    }
    #footer p {
        font-size: .9rem;
    }
    .highlighted {
        color: var(--light-blue);
        font-weight: 600;
    }
</style>