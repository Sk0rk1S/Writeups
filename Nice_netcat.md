# Instructions: Connect to the host wily-courier.picoctf.net at port 50457 using netcat

I accomplished connecting to the port and hostnumber by using the nc(netcat) command in the format: nc {HOSTNAME} {PORT_NUMBER}
which was: nc wily-courier.picoctf.net 50457

After connecting, the program spits out the following series of ASCII characters: 
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
56 
51 
54 
57 
49 
125 
10

# Decoding the Ascii Characters

I spent way too long on this problem because I couldnt find a website that would sucessfully convert these Ascii values to plaintext
so I gave up and did it myself

(The better way was to Use CyberChef.io with the recipe "from Decimal" and paste the numbers)

The program used to decode the Ascii characters:

public class Flag
{
  public static void main(String[] args)
  {
  int[] Ascii = {112, 
  105, 
  99, 
  111, 
  67, 
  84, 
  70, 
  123, 
  103, 
  48, 
  48, 
  100, 
  95, 
  107, 
  49, 
  116, 
  116, 
  121, 
  33, 
  95, 
  110, 
  49, 
  99, 
  51, 
  95, 
  107, 
  49, 
  116, 
  116, 
  121, 
  33, 
  95, 
  56, 
  51, 
  54, 
  57, 
  49, 
  125, 
  10};
  
  String flaG = "";
  
  for(int i = 0; i < Ascii.length; i++)
  
  {
  
    flaG += (char)Ascii[i];
  }
  
  System.out.println(flaG);
  
  }
  
}

Finally I found the flag: picoCTF{g00d_k1tty!_n1c3_k1tty!_83691}

