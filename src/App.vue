<script>
export default{
    data: function () {
        return {
            token: null,
            some_data: null,
            errormsg: null,
			dataBool: false,
        }
    },
    methods:{
        async info(){
			// let response = await this.$axios.get("/");
			// this.some_data = response.data;

        },
    },
    async mounted(){
        await this.info()
    }

}
</script>
<template>
    <header>
        <hgroup>
            <h1>MicroAlgae DB</h1>
        </hgroup>
        <nav>
            <ul class="right">
                <li>
                    <RouterLink to="/">
                        Home
					</RouterLink>
                </li>
                <li>
                    <RouterLink to="/">
                        About Vulgaris
					</RouterLink>
                </li>
            </ul>
            <ul class="left">
                <li>
                    <RouterLink to="/taxonomy">
                        Taxonomy
					</RouterLink>
                </li>
                <li>
                    <RouterLink to="/taxon">
                        Search
					</RouterLink>
                </li>

                <li>
                    <RouterLink to="/sra">
                        SRA
					</RouterLink>
                </li>

            </ul>
        </nav>
    </header>
    <RouterView />
    <footer>
        <div id="banner" style="overflow:hidden; display: inline-block;">
            <div class="image">
                <img src="/images/Stemma_sapienza.png" style="width:30%; height:30%">
            </div>
        </div>
        <p>Authors: Team di Biologia Computazionale 2023, Università La Sapienza<br>
        </p>
        <div style="margin-top: 12px;">
            <a href="mailto:">bio@bio.it</a>
            <a href="https://github.com/BITSapienza" style="margin-left: 40px;">BIT Sapienza</a>
        </div>
    </footer>
</template>

<style>
</style>
