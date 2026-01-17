# Instructions: Connect to the host wily-courier.picoctf.net at port 50457 using netcat
I accomplished connecting to the port and hostnumber by using the nc(netcat) command in the format: nc {HOSTNAME} {PORT_NUMBER}
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
Using an Ascii to plaintext converter (cyberchef.io), I was able to obtain the following: picoCTF{g00d_k1tty!_n1c3_k1tty!_83691}
