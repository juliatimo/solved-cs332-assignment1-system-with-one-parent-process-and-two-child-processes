Download Link: https://assignmentchef.com/product/solved-cs332-assignment1-system-with-one-parent-process-and-two-child-processes
<br>
One of the philosophies behind Unix is the motto <u>do one thing and do it well</u>. In this spirit, each shell command usually has a very specific purpose. More complicated commands can be constructed by combining simpler commands in a <u>pipeline</u> such that the output of one command becomes the input to another command. The standard shell syntax for pipelines is to list multiple commands, separated by vertical bars  (the pipe character).




Your task is to create a system with one parent process and two child processes where the children communicate using a pipe.




<table width="628">

 <tbody>

  <tr>

   <td colspan="3" width="299">In the below example the output from the</td>

   <td width="51">ls -F</td>

   <td colspan="3" width="278"> command is piped to input of</td>

  </tr>

  <tr>

   <td rowspan="3" width="31">the</td>

   <td width="19"> </td>

   <td colspan="5" rowspan="3" width="578"> command.</td>

  </tr>

  <tr>

   <td width="19">nl</td>

  </tr>

  <tr>

   <td width="19"> </td>

  </tr>

  <tr>

   <td colspan="5" width="523">Use fork(), one form of exec() functions, so that the first child will perform</td>

   <td width="51">ls -F</td>

   <td width="53"> and</td>

  </tr>

  <tr>

   <td width="31"></td>

   <td width="19"></td>

   <td width="249"></td>

   <td width="51"></td>

   <td width="174"></td>

   <td width="51"></td>

   <td width="53"></td>

  </tr>

 </tbody>

</table>

pass the output to the second child using one direction pipe, so the second one can

<table width="628">

 <tbody>

  <tr>

   <td width="64">perform</td>

   <td width="19">nl</td>

   <td width="545">  on the list of current directory contents. Later the second child process will</td>

  </tr>

  <tr>

   <td colspan="3" width="628">print to the screen the result (see example below). The parent process must wait for its</td>

  </tr>

 </tbody>

</table>

both children.

<table width="244">

 <tbody>

  <tr>

   <td width="46">1</td>

   <td width="198">file1*</td>

  </tr>

  <tr>

   <td width="46">2</td>

   <td width="198">file2*</td>

  </tr>

  <tr>

   <td width="46">3</td>

   <td width="198">dir1/</td>

  </tr>

  <tr>

   <td width="46">4</td>

   <td width="198">dir2/</td>

  </tr>

 </tbody>

</table>







Submit the following:

<ol>

 <li>Your complete code with all comments</li>

 <li>Screenshot of the output (suggesting to create few files and directories within the assignment local directory)</li>

</ol>

<ul>

 <li>Assignment report which will answer the following questions:

  <ol>

   <li>What form of exec() function you used? Why?</li>

   <li>How many times you used fork? Why?</li>

   <li>How many pipes this assignment required? Why?</li>

   <li>What form of wait() you used? How many times?</li>

  </ol></li>

</ul>