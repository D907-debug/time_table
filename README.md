# Ex03 Time Table
# Date:30/10/24
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using <table> tag in html.

## STEP 4
Add header row using <th> tag.

## STEP 5
Add your timetable using <td> tag.

## STEP 6
Execute the program using runserver command.

## PROGRAM
~~~
from django.shortcuts import render,HttpResponse
def trail(request):
    return HttpResponse('<p>hello</p>')
def htm(request):
    return render(request,"home.html")
content = ''' 
<!DOCTYPE html>
<head>

   <TITle>WEB DEVELOPMENT</TITle><center>

<img  style="height: 150px; width: 800px;" src="C:\Users\admin\Desktop\new\web\app\sav.png" alt="saveetha">    
<hr>
<h1> SLOT TIME TABLE</h1></center>
</head>
<BODY>
    <marquee>K.DILLI BABU [24900561] SAVEETHA ENGINEERING COLLEGE</marquee>
    <center>
        <table style="height: 250px; width: 700px;" class="timetable" border="10px">
            <tr>
                <th style="background-color: yellow;">DAY</th>
            <th style="background-color: yellow;">PERIOD-1 </th>
            <th style="background-color: yellow;">PERIOD-2</th>
            <th   rowspan="7">LUNCH</th>
            <th style="background-color: yellow;">PERIOD-3</th>
            </tr>
            <tr>
                <td style="background-color: yellow;">MONDAY</td>
                <td style="background-color:blue;">-</td>
                <td style="background-color: blue;">BEEE</td>
                <TD style="background-color: blue;">WEB DEVELOPMENT</TD>
            </tr>
            <TR>
                <TD style="background-color: yellow;">TUESDAY</TD>
                <TD style="background-color: blue;">COM ENGLISH</TD>
                <TD style="background-color: blue;">BEEE</TD>
                <TD style="background-color: blue;">C PROGRAM</TD>
                
            </TR>
            <TR>
                <TD style="background-color: yellow;">WEDNESDAY</TD>
                <TD style="background-color: blue;">-</TD>
                <TD style="background-color: blue;">IOT</TD>
                <TD style="background-color: blue;">-</TD>
            </TR>
            <TR>
                <TD style="background-color: yellow;">THURSDAY</TD>
                <TD style="background-color: blue;">PHYSICS</TD>
                <TD style="background-color: blue;">WEB DEVELOPMENT</TD>
                <TD style="background: blue;">C PROGRAM</TD>
            </TR>
            <TR>
                <TD style="background-color: yellow;">FRIDAY</TD>
                <TD style="background-color: blue;">COM ENGLISH</TD>
                <TD style="background-color: blue;">WEB DEVELOPMENT</TD>
                <TD style="background-color: blue;">PHYSICS</TD>
            </TR>
            <TR>
                <TD style="background-color: yellow;">SATURDAY</TD>
                <TD style="background-color: blue;">-</TD>
                <TD style="background-color: blue;">WEB DEVELOPMENT</TD>
                <TD style="background-color: blue;">IOT</TD>
            </TR>

        </table>
    </tr>
    <table style="height: 250px; width: 700px;" class="timetable" border="10px">
        <tr>
            <td>S.No</td>
            <td>SUBJECT CODE</td>
            <td>Subject Name</td>
        </tr>
        <tr>
            <td>1.</td>
            <td>19AI304</td>
            <td>Fundamentals of C programming</td>
        </tr>
        <tr>
            <td>2.</td>
            <td>19AI414</td>
            <td>Fundamentals of Web Development</td>
        </tr>
        <tr>
            <td>3.</td>
            <td>19CS420</td>
            <td>Prototyping of IOT</td>
        </tr>
        <tr>
            <td>4.</td>
            <td>19EE404</td>
            <td>Digital Electronics</td>
        </tr>
        <tr>
            <td>5.</td>
            <td>19EN101</td>
            <td>Communicative English</td>
        </tr>
        <tr>
            <td>6.</td>
            <td>SH3214</td>
            <td>Physics For Quantum Computing</td>
        </tr>
        <tr>
            <td>7.</td>
            <td>19EE305</td>
            <td>Measurement Engineering</td>
        </tr>
        
    </table>
</center>
</BODY>

  </html>
  '''


from http.server import HTTPServer,BaseHTTPRequestHandler
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',8000)
httpd = HTTPServer(server_address,Myserver)
httpd.serve_forever()


~~~
## OUTPUT
![image](https://github.com/user-attachments/assets/481ec09c-e9e1-4c53-a07a-c76f903dabb8)
![image](https://github.com/user-attachments/assets/e2927cee-04b8-4b19-aab5-c55d3bdfb0c7)

## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
