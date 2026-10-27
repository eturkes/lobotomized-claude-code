<!--
name: 'Tool Description: save_task_files'
description: >-
  Description of the save_task_files tool that saves a task's produced files to
  this computer under their listed names, with approval for every call
ccVersion: 2.1.310
variables:
  - TOOL_DESCRIPTION_SAVE_TASK_FILES_VAR_0
-->
Save files that a task produced to this computer. Pass the task's task_id and, for up to ${TOOL_DESCRIPTION_SAVE_TASK_FILES_VAR_0} of its files, the file's id, the name it is saved as and its size in bytes, each exactly as a get_task answer for that task gave them earlier in this session: the saved-as name is the name the task gave the file, made safe as a file name, and the answer's note spells it out where the two differ or the name is long. Each file is saved in this session's task-files folder under that name, with a number added if the name is taken; nothing is overwritten. The person is asked to approve every call. The answer says where each file was saved, or why it was not.
