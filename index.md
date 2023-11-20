<div style="background-color:#d1aef2;">
  
<h3 style="font:Arial Black;"> Lab Report 4 </h3>
<p style="font:Tahoma;"> November 18, 2023</p>

<h4 style="font:Tahoma;"> Vim Steps From Lab</h4>
 <ol>
  <li><h4 style="font:Tahoma;">Log into ieng6</h4>
    <table>
  <tr>
   <td> <p style="font:Tahoma;">Keys pressed: <code>ssh cs15lfa23zz@ieng6.ucsd.edu</code></p> 
        <p><i>The <code>ssh</code> command allows the use<br> 
          to establish a connection from their personal <br>
          computer to a network. In this case,<br>
          the command established a connection to the <br>
          <code>ssh cs15lfa23zz@ieng6.ucsd.edu</code> server.</i></p>
   </td>
    <td> <img src="Screen Shot 2023-10-20 at 4.13.39 PM.png"> </td>
  </tr>
    </table>
  </li>

  <li><h4 style="font:Tahoma;">Clone your fork of the repository from your Github account (using the <code>SSH</code> URL)</h4>
    <table>
  <tr>
   <td> <p style="font:Tahoma;">Keys pressed: <code>git clone git@github.com:loethan10/lab7-1.git</code></p> 
        <p><i>The <code>git clone</code> command does what it<br>
          implies- it clones a copy of the git provided. <br>
          In this case, the command cloned what was at <br>
          the <code>git@github.com:loethan10/lab7-1.git</code> URL. <br>
          Note that the aforementioned directory cloned<br>
          was provided by using an SSH code that was established <br>
          during lab.</i></p>
   </td>
    <td> <img src="Screen Shot 2023-10-20 at 4.13.39 PM.png"> </td>
  </tr>
    </table>
  </li>
  
  </li>
  <li>Run the tests, demonstrating that they fail</li>
  <li>Edit the code file <code>ListExamples.java</code> to fix the failing test (as a reminder, the error in the code is just that <code>index1</code> is used instead of <code>index2</code> in the final loop in <code>merge</code>)</li>
  <li>Run the tests, demonstrating that they now succeed</li>
  <li>Commit and push the resulting change to your Github account</li>
 </ol>
 </div>
 
 
 
 
 
 
 
 
 
 
 
 
 
 <div style="background-color:#8bf76a;">
  
<h3 style="font:Arial Black;"> Lab Report 3 </h3>
<p style="font:Tahoma;"> November 2, 2023</p>

<h4 style="font:Tahoma;"> Part 1 </h4>
<p style="font-size: 12 px">Fixing the bugs within the code for a list implementation: </p>
<p style="font-size: 12 px">For this portion, we will be looking at the list's method <code>reverseInPlace</code></p>
<pre style = "background-color: #96948f"><code>static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
} </code></pre>
   
<ul style="font:Tahoma;">
   <li>Failure-inducing input for the buggy program:</li>
</ul>
   <pre style = "background-color: #96948f"><code>@Test 
public void testReverseInPlaceAccurately() {
   int[] input1 = {3, 4, 5, 6, 7};
   ArrayExamples.reverseInPlace(input1);
   assertArrayEquals(new int[]{7, 6, 5, 4, 3}, input1);
}</code></pre>
 <ul style="font:Tahoma;">
   <li>Input that doesn’t induce a failure:</li>
 </ul>
   <pre style = "background-color: #96948f"><code>@Test 
public void testReverseInPlacePoorly() {
   int[] input1 = {3};
   ArrayExamples.reverseInPlace(input1);
   assertArrayEquals(new int[]{3}, input1);
}</code></pre>
<ul style="font:Tahoma;">
   <li>Test results:</li>
</ul>
   <img src="Screen Shot 2023-11-03 at 11.19.01 PM.png">
    <table align="center" style="margin: 0 px auto;">
  <tr>
    <td>
     <pre style = "background-color: #96948f"><code>static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}</code></pre></td>
    <td>
     <pre style = "background-color: #96948f"><code>static void reverseInPlace(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[i];
    }
  }</code></pre>
    </td>
  </tr>
  <tr>
    <td> <p>Code before</p></td>
    <td> <p>Code after</p></td>
  </tr>
    </table>
<p>The initial code for <code>reverseInPlace</code> overwrote the first half of the array without storing its information, causing the inital values in the first half of the array to disappear. This resulted in a palindromic array. The code for the method actually stores the information into a temporary array, and then changes the values, accordingly, so that the initial values are not immediately overwritten.</p>
     
<h4 style="font:Tahoma;"> Part 2 </h4>
<p>For this part, we will be focusing on the terminal command <code>less</code>. Note that for the following four command-line options, I found them through the URL: "<a href="https://phoenixnap.com/kb/less-command-in-linux">https://phoenixnap.com/kb/less-command-in-linux</a>."</p>
<ol>
  <li><code>-o[file_name]</code>: this command-line copies the output into a specified file</li>
 <table align="center" style="margin: 0 px auto;">
  <tr>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less ./technical/911report/chapter-1.txt 
      | less -o input.txt</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>Warning: "input.txt" exists; 
     Overwrite, Append or Don't log? 
Overwrite, Append, or Don't log? (Type "O", "A", "D" or "q")</code></pre></p>
    </td>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less ./technical/911report/ 
      | less -o input.txt</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>./technical/911report/ is a directory
Warning: "./technical/911report/" exists; 
     Overwrite, Append or Don't log? 
Cannot write to "./technical/911report/"</code></pre></p>
    </td>
  </tr>
  <tr>
    <td> <p>Here, before <code>|</code>, we call a command. Then, we input that command's output into a file called <code>input.txt</code>. After letting the command run and allowing the terminal to overwrite <code>input.txt</code>'s initial data, <code>less</code> proceeds to print the output both on the terminal space and in the txt file.</p></td>
    <td> <p>Here, the command before <code>|</code> executes, as normal, again. However, because <code>-o</code> is now taking a directory as the target to overwrite, the terminal fails to do anything. It outputs an error message, since it requires a file as an argument, not a directory.</p></td>
  </tr>
    </table>
     
  <li><code>-p[pattern]</code>: this command-line causes <code>less</code> to start searching at the first instance specified pattern</li>
  <table align="center" style="margin: 0 px auto;">
  <tr>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less -p help ./technical/911report/chapter-1.txt</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f">
<code>...help the FAA centers coordinate directly with the 
 military. NORAD would receive tracking
information for the hijacked aircraft either from 
 joint use radar or from the relevant FAA air
traffic control facility. Every attempt would be 
 made to have the hijacked aircraft squawk 7500 to
help NORAD track it...</code></pre></p>
    </td>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less -p help ./technical/biomed/</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>../technical/biomed/ is a directory</code></pre></p>
    </td>
  </tr>
  <tr>
    <td> <p><code>less</code> does what it normally does, which is printing out the contents of the given file to the terminal. However, given the specified command <code>-p</code>, with the string <code>help</code>, the command searches for the first instance of the pattern, then jumps to that part of the file (making it the first thing the user sees).</p></td>
    <td> <p>Because <code>less -p</code> requires a file as an input, the terminal sends out an error message when passed a directory, instead of a file.</p></td>
  </tr>
    </table>
     
  <li><code>-z[number]</code>: this command-line simply reformats the output window to show a specified number of lines</li>
  <table align="center" style="margin: 0 px auto;">
  <tr>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less -z 10 ./technical/911report/chapter-1.txt</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>
        
                
"WE HAVE SOME PLANES"

   Tuesday, September 11, 2001, dawned temperate and nearly 
   cloudless in the eastern United States. 
   Millions of men and women readied themselves for work. 
   Some made their way to the Twin Towers, the 
   signature structures of the World Trade Center 
   complex in New York City. Others went to Arlington, 
   Virginia, to the Pentagon. Across the Potomac River, 
   the United States Congress was back in session. At 
   the other end of Pennsylvania Avenue, people began to 
   line up for a White House tour. In Sarasota, 
   Florida, President George W. Bush went for an 
   early morning run.</code>
   </pre></p>
    </td>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less -z 1 ./technical/biomed/</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>./technical/biomed/ is a directory</code></pre></p>
    </td>
  </tr>
  <tr>
    <td> <p><code>less</code> does what it normally does, which is printing out the contents of the given file to the terminal. However, given the specified command <code>-z</code>, with the number value <code>10</code>, the command prints out 10 lines at a time.</p></td>
    <td> <p>Because <code>less -z</code> requires a file as an input, the terminal sends out an error message when passed a directory, instead of a file.</p></td>
  </tr>
    </table>
     
  <li><code>-N</code>: this command-line simply shows the line numbers at the side of the screen</li>
  <table align="center" style="margin: 0 px auto;">
  <tr>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less -N ./technical/911report/chapter-1.txt</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>1 
      2         
      3                 
      4 "WE HAVE SOME PLANES"
      5 
      6     Tuesday, September 11, 2001, dawned temperate and 
     nearly cloudless in the eastern United States.</code></pre></p>
    </td>
    <td>
     <p>Command:<pre style = "background-color: #96948f"><code>less -N ./technical/biomed/</code></pre></p>
    <p>Output:<pre style = "background-color: #96948f"><code>./technical/biomed/ is a directory</code></pre></p>
    </td>
  </tr>
  <tr>
    <td><p><code>less</code> does what it normally does, which is printing out the contents of the given file to the terminal. However, given the specified command <code>-N</code>, the command also prints out the lines number to the left of the screen.</p></td>
    <td> <p>Because <code>less -N</code> requires a file as an input, the terminal sends out an error message when passed a directory, instead of a file.</p></td>
  </tr>
    </table>
</ol>
</div>
 
 
 
 
 
 
 






 
 
 
 <div style="background-color:#87CEFA" width = "1300">
  
<h3 style="font:Arial Black;"> Lab Report 2 </h3>
<p style="font:Tahoma;"> October 19, 2023</p>

<h4 style="font:Tahoma;"> Part 1 </h4>
  <table>
  <tr>
    <td> <img src="Screen Shot 2023-10-20 at 4.16.17 PM.png"></td>
    <td> <img src="Screen Shot 2023-10-20 at 4.19.50 PM.png"></td>
  </tr>
  <tr>
    <td> <p> The image shown is a screenshot of the server being run. It has taken several strings as an argument ("Hello," "Never," "Gonna," "Give," etc) and concatenated them to a long String, which is implemented to look visually similar to a list. The server utilizes a Java class called StringServer, where it is calling a method <code>handleRequest</code>, which takes a URL as an argument, then parses the URL into several Strings to decode it. The method searches for the String "add-message" after the "/" character, which then looks for a "?=" combination of characters. From there, the rest of the URL is a String that the method uses as an argument to pass to a variable that keeps a running list of all previous Strings passed to the method. When updating the list, a String variable (that holds the list) and an int variable (that keeps track of how many Strings have been passed) are updated. </p></td>
    <td> <p>Similar to the other image, this screenshot shown is one of the server. In this case, however, the server sends out an error statement, since it did not find any valid inputs to either update the running list or to simply show it. The handleRequest method is still called, but since no valid arguments were passed, it returns the statement "404 Not Found!" Furthermore, as a result, no variables were changed.</p></td>
  </tr>
</table>
<h4 style="font:Tahoma;"> Part 2 </h4>
  <table>
  <tr>
    <td> <img src="Screen Shot 2023-10-20 at 4.13.39 PM.png"> </td>
    <td> <img src="Screen Shot 2023-10-20 at 4.50.37 PM.png"></td>
  </tr>
  <tr>
    <td> <p style="font-size: 12 px; color: gray">Code for <code>StringServer</code></p></td>
    <td> <p> Logging into ieng6 without the need for my password </p></td>
  </tr>
    <tr>
    <td> <img src="Screen Shot 2023-10-20 at 4.49.02 PM.png"></td>
    <td> <img src="Screen Shot 2023-10-20 at 4.53.19 PM.png"></td>
    </tr>
    <tr>  
    <td> <p> The path to the private key for my SSH key on my computer </p></td>
    <td> <p> The path to the public key for my SSH key on the ieng6 computer/server </p></td>
    </tr>
</table>
<h4 style="font:Tahoma;"> Part 3 </h4>
  <p style="font:Tahoma;"> I learned many things this week, but the thing that stood out to me most were all the little shortcuts you could use to navigate and/or type commands much faster on the terminal. For example, I learned that control + C (or command, depending on keybinds) stops a server, allowing you to continue typing onto the terminal; this was something I critically needed, as I kept accidentally "softlocking" myself out of the terminal, as I didn't know how to stop a command. Also, I learned that using the up/down arrow keys allows me to re-run commands from before, saving me the hassle of having to retype a command, with a potential typo. Finally, I learned that control + A allows me to go back to the beginning of a line.</p>



</div>








<div style="background-color:#FFEBCD">
  
<h3 style="font:Arial Black;"> Lab Report 1 </h3>
<p style="font:Tahoma;"> October 3, 2023</p>

<h4 style="font:Tahoma;"> Terminal Commands </h4>
<p style="font:Tahoma;"> For week 1's lab, we learned how to use Edstem, a workspace, which has a terminal that we can use to run commands. Three of these such commands are <code>cd</code>, <code>ls</code>, and <code>cat</code>.</p>

<ul style="font:Tahoma;">
  <li><b><code>cd</code></b></li>
  
  <table>
  <tr>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-22 at 4.06.20 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.37.49 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.40.01 PM.png"></div></td>
  </tr>
  <tr>
    <td> <div style="length: 620 px">This is an example of using the command <code>cd</code> with no arguments. The working directory was <code>/home/lecture1/messages</code>. Since there was no argument, <code>cd</code> changed the working directory back to <code>/home</code>. The lack of output is intentional, and there is no error, as the directory was changed.</div></td>
    <td> <div style="length: 620 px">This is an example of using the command cd on a path to a directory as an argument. In this example, cd changed the working directory from <code>/home</code> to <code>/home/lecture1</code>. The lack of output is intentional, and there is no error, as the directory sucessfully changed. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command <code>cd</code> on a path to a file as an argument. The current working directory is <code>/home/lecture1</code>. However, since <code>cd</code> needs a directory as an argument (to change the directory into whatever was entered), the command produced an error; both inputs in the example above are files, not directories. </div></td>
  </tr>
</table>
  
  <li><b><code>ls</code></b></li>

<table>
  <tr>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.40.40 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.41.11 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.41.38 PM.png"></div></td>
  </tr>
  <tr>
    <td> <div style="length: 620 px">This is an example of using the command <code>ls</code> with no arguments. The command outputs all the files and directories (essentially the contents) within the current directory, which is <code>/home/lecture1</code>. Because there are no arguments, the command outputs the contents of the current directory, by default. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command <code>ls</code> on a path to a directory as an argument. The current directory is <code>/home/lecture1</code>, but since we input <code>/home/lecture1/messages</code> as the input, the command instead prints the directory contents of the input. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command <code>ls</code> on a path to a file as an argument. The current directory is <code>/home/lecture1</code>; normally, the command would print its contents, by default. However, since we used a file as the input, the command only prints out the file itself (as it's the only content within it). </div></td>
  </tr>
</table>

  <li><b><code>cat</code></b></li>

<table>
  <tr>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-22 at 4.12.12 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.43.42 PM.png"></div></td>
    <td> <div style="length: 620 px"><img src="Screen Shot 2023-10-04 at 4.44.24 PM.png"></div></td>
  </tr>
  <tr>
    <td> <div style="length: 620 px">This is an example of using the command <code>cat</code> with no arguments. The current directory is simply <code>/home</code>. The command produced no error; this specific terminal stopped accepting further command inputs, and instead printed whatever text the user typed into the terminal. This is not an error, as cat reads data as input, then prints data as output. </div></td>
    <td> <div style="length: 620 px">This is an example of using the command <code>cat</code> on a path to a directory as an argument. The current directory is <code>/home</code>. In the command, we used the directory <code>/lecture1</code> as an argument. This produced an error, as cat requires files to print out an output.</div></td>
    <td> <div style="length: 620 px">This is an example of using the command <code>cat</code> on a path to a file as an argument. The current directory is <code>/home</code>, and we are using <code>/lecture1/Hello.java</code> as a file input. This successfully produces an output, which is the contents of the <code>Hello.java</code> file.</div></td>
  </tr>
</table>
  
</ul>

</div>
