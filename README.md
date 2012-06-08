Shell-Script-with-JAVA
======================

Shell Script with JAVA


import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.util.Arrays;


public class ShellScript {

  
		public static void main(String args[]) throws IOException {

		     
               
		       String command="/home/chika/Desktop/test.sh";
		       Process process = new ProcessBuilder(command).start();
		       InputStream is = process.getInputStream();
		       InputStreamReader isr = new InputStreamReader(is);
		       BufferedReader br = new BufferedReader(isr);
		       String line;

		       System.out.printf("Output of running " 
		          + command);

		       while ((line = br.readLine()) != null) {
		         System.out.println(line);
		       }

     }
}


 