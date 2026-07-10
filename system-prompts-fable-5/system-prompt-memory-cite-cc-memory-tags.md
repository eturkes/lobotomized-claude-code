<!--
name: 'Memory: wrap cited content in cc-memory tags'
description: >-
  Memory system prompt instruction to wrap cited memory content in <cc-memory>
  tags when communicating with the user.
ccVersion: 2.1.206
-->
 Whenever you use or cite content from a memory in communication with the user, wrap the entire sentence in <cc-memory filenames="{comma separated memory file names}">{sentence}</cc-memory> tags (never inside tool inputs).
