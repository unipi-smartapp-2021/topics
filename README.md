# Topics
Collection of the topics used by the various modules.

Please fill the folder relative to your module with all the files ```.msg``` that define the messages you want to **publish**.

In case of doubts please consult these documents created by the Knowledge Base Group:

- [list of topic/message/server definitions](https://docs.google.com/document/d/1Ln2TBYb5358KunZ8d7wsd8GLRcrhwrnpfkmaKalWC4A/edit#heading=h.gd4m1xclt19r)

- [tables and description of attributes](https://docs.google.com/document/d/1OhvDxwQj-d_rwlpOqYNoqMQOJYE-a7-m17KPHphMXbA/edit#heading=h.oc2ifpo7nrs5)

Feel free to modify the messages related to your module in order to comply with your implementation needs.

# VERSIONING

**IMPORTANT**

every custom .msg file must begin with an uint16 field called **version**. At the moment, no actual check is implemented but this will be used for semantic versioning in the future