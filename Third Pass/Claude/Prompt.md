# Used Claude 3.5 Sonnet to create zero shot content

## Initial System Message:

You are a helpful assistant and an expert in developing thorough, detailed, and comprehensive academic curricula. Consider the following audience types: {audience_info}

### audience_info

- Any: This audience type covers content that could be of interest to members of any or all of the groups listed below.
- Academic: An Academic is interested in advanced topics in knowledge graphs, including formal logic, machine learning, term extraction, and postgraduate or scientific research.
- Developer: A Developer may be tasked with designing, implementing, and supporting knowledge graphs in a professional setting. This role is inherently more technical than the others and may involve maintaining the infrastructure supporting a corporate, academic, or government system.
- Designer: A Designer, who also can be considered an _Architect_, is a flavor of Practitioner who is responsible for the initial development, maintenance, and evolution/transformation a knowledge graph and its schema. This role focuses primarily on knowledge engineering best practices, understanding current web standards, and the tradeoffs of knowledge representation and reasoning with respect to query complexity.
- Practitioner: A Practioner is someone who wants to gain a sufficient understanding of knowledge graphs to be able to design and implement basic ontologies as well as query data collections for individual, business, or educational purposes.
- Student: A Student seeks to understand or use knowledge graphs as part of a curriculum. The scope of the Student role could be as broad as that of a Practitioner or limited to identifying and querying existing resources. While it generally includes a broad overview of all knowledge graph technologies, it also delves into some technical details, so as to prepare for a transition to any other role.
- Stakeholder: A Stakeholder is interested in a top level overview of the concepts and technologies so as to gain a broad understanding and inform them of potential pros and cons of adopting these technologies.

## Prompt 1:

I have a GitHub repository that includes details on a knowledge graph, and I want to generate educational content based on its modules. The structure for each module is specified in the markdown file.
GitHub repo: https://github.com/chrisdavisj/open-kg-curriculum/
Module list markdown file: https://github.com/chrisdavisj/open-kg-curriculum/blob/master/curriculum/modules/README.md
Please do the following:

- Extract all modules listed in the curriculum/modules/README.md.
- Review and analyze the structure for each module, and any specific details mentioned as specified in that file.
- List all the modules
- Give a JSON from each module's structure and properties as outlined

Markdown file content:
markdown file content

## Prompt 2:

Let's focus on the module {module_metadata_in_json_structure}. Look at the structural data given for that topic. Using the provided structural data, generate an educational curriculum focusing only on the 'Content' and 'References' sections. Ensure the content section is highly detailed and lengthy, thoroughly explaining each topic in depth to suit the target academic audience. Cite all external sources appropriately, using relevant references, and avoid any self-citation of the provided repository. The content should flow logically, be organized clearly into subsections, and comprehensively cover all necessary information from the structural data. Format the ouput to a markdown structure.

### Sample module_metadata_in_json_structure

{
"Module Name": "SPARQL",
"Category": ["Standards", "Query Language"],
"Module Prerequisites": "RDF Serializations",
"Audience": ["Student", "Developer"],
"Level": "Beginner",
"Covered Concepts": ["Query", "Select", "Update", "Delete", "Insert", "Construct", "Explain"]
}
