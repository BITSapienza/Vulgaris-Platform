<script>
export default {
	props: ['data'],
    methods:{
    }
}
</script>

<template>
    <!-- <div>BioProjects of {{ scientificName }}</div> -->
    <tr>
        BioProjects of {{ data[0].ScientificName ? data[0].ScientificName : data[0].TaxId }}
    </tr>
    <ul v-for="proj in data">
        <div class="origin">
            BioProject: ({{ proj.BioSamples.length }})
        </div>
        <div class="clickable">
            {{ proj.BioProjectId }}
        </div>
        <ul>
            <tr>
                <td v-for="sample in proj.BioSamples">
                    <div class="origin">
                        BioSample: ({{ sample.Experiments.length }})
                    </div>
                    <div class="clickable">
                        {{ sample.BioSampleId }}
                    </div>
                    <ul>
                        <tr>
                            <td v-for="exp in sample.Experiments">
                                <div class="origin">
                                    Experiment: ({{ exp.Runs.length }})
                                </div>
                                <div class="clickable">
                                    {{ exp.ExperimentId }}
                                </div>
                                <ul v-for="run in exp.Runs">
                                    <tr>
                                        <td>
                                            <div class="origin">
                                                Run:
                                            </div>
                                            <div class="clickable">
                                                {{ run }}
                                            </div>
                                        </td>
                                    </tr>
                                </ul>
                            </td>
                        </tr>
                    </ul>
                </td>
            </tr>
        </ul>
        <div v-if="proj.ImagesPath && proj.ImagesPath.length > 0" class="immagini">
            <div v-for="img in proj.ImagesPath">
                <img :src="img" alt="Prova">
            </div>
        </div>
    </ul>
    
</template>

<style>
.origin{
    color: rgb(172, 172, 172);
}
</style>