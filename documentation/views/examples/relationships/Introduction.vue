<template>
    <div>
        <h2 class="markdown-header">Relationships</h2>
        <information-alert>
            The current implementation requires that you disable ONLY_FULL_GROUP_BY in your database configuration.
            
            Run <code>php artisan config:cache</code> after making your changes to your database configuration.
            <br><br>
            If you cannot turn off strict mode or are unable to remove the ONLY_FULL_GROUP_BY configuration. You can still make use of this packing using your own Eloquent or QueryBuilder queries and by paginating the results for the Datatable Collection Resource.
        </information-alert>
        <pre>
            <my-sql-config>
            </my-sql-config>
        </pre>

        <h2 class="markdown-header">Adding Relationships</h2>
        <pre>
            <relationship-markdown>
            </relationship-markdown>
        </pre>
    </div>
</template>

<script>

    import Prism from 'prismjs';
    import CorrectTextStyling from '../../../mixins/CorrectTextStyling';
    import InformationAlert from '../../../example-components/InformationAlert.vue';
    import MySqlConfig from '../../../markdown/examples/relationships/mysql-config.md';
    import RelationshipMarkdown from '../../../markdown/examples/relationships/introduction.md';
    
    export default {
        name: 'Relationships-Introduction',
        mixins: [CorrectTextStyling],
        components: {
            RelationshipMarkdown,
            InformationAlert,
            MySqlConfig
        },
        mounted() {
            this.$nextTick(Prism.highlightAll);
        },
    }
</script>
