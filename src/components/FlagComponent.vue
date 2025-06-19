<template>
    <div class="hello">
        <h2>{{ title }}</h2>
        <!-- Use v-html with formatted paragraphs -->
        <div class="description" v-html="formattedDescription"></div>
        <img :src="require(`@/assets/${image}`)" :alt="alt" />
    </div>
</template>

<script>
export default {
    name: 'FlagComponent',
    props: {
        title: String,
        image: String,
        alt: String,
        description: String,
    },
    computed: {
        formattedDescription()
        {
            // Convert newlines to <p> tags or <br>
            return this.description
                .split('\n\n') // Split by double newlines for paragraphs
                .map(paragraph => paragraph.trim())
                .filter(paragraph => paragraph.length > 0)
                .map(paragraph => `<p>${paragraph.replace(/\n/g, '<br>')}</p>`)
                .join('');
        }
    }
}
</script>

<style scoped>
.description {
    text-align: left;
    max-width: 800px;
    margin: 0 auto;
    line-height: 1.6;
}

.description p {
    margin-bottom: 1em;
}

.description ul {
    padding-left: 20px;
    margin: 10px 0;
}

.description li {
    margin-bottom: 5px;
}
</style>