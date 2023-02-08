`ssh cs15lwi23ady@ieng6.ucsd.edu`

Run JUnit:

`local $ javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java`
 
`local $ java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore XXXTests`

Find how many txt files:

`find written_2 > find-results.txt`

`grep ".txt" find-results.txt > grep-results.txt`

`wc grep-results.txt`

find the file in the data directory that contains the string "Lucayans":

`grep -rl "Lucayans" written_2`

Start Server:

`javac Server.java FileServer.java `

`java FileServer`

`java FileServer 1206 ../skill-demo1-data`

`http://ieng6-202:1206/`

`http://ieng6-202:1206/search?q=Bahamas-History`

`http://ieng6-202:1206/search?q=Bahamas`
