# Output file and directory structures to HTML, JSON and XML using the Linux tree command

[Tree][1] is a recursive directory listing command that produces a depth indented listing of files, which is colorized ala dircolors if the LS_COLORS environment variable is set and output is to tty. Tree has been ported and reported to work under the following operating systems: Linux, FreeBSD, OS X, Solaris, HP/UX, Cygwin, HP Nonstop and OS/2. 

## Tree Options
Tree has a vast array of options and I've gone through each of them to fine-tune and perfect the outputs for HTML, JSON and XML formats. To see a list of available options simply run `tree --help` from your terminal.

Below is a list of only the options I used to create workable formats for HTML, JSON and XML data formats.

 * `-o filename`: Output to a file instead of stdout.
 * `-h`: Print the size in a more human readable way.
 * `-D`: Print the date of last modification or (-c) status change.
 * `-C`: Turn colorization on always.
 * `-X`: Prints out an XML representation of the tree.
 * `-J`: Prints out an JSON representation of the tree.
 * `-H baseHREF`: Prints out HTML format with baseHREF as top directory.

## HTML Output
```bash
$ tree -hDC -H /Users/macbookpro/acme.sh /Users/macbookpro/acme.sh -o acme.html
```
This will produce the following output in HTML format.

![HTML Output](https://i.snag.gy/ufLSeZ.jpg)

## XML Output
```bash
tree -hDC -X /Users/macbookpro/acme.sh -o acme.xml
```
This will produce the following output in XML format.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<tree>
  <directory name="/Users/macbookpro/Justin">
    <directory name="Dirs" size="160" time="Jan 30 14:12">
      <directory name="One" size="128" time="Jan 30 14:13">
        <directory name="Two" size="160" time="Jan 30 14:13">
          <directory name="Three" size="320" time="Jan 30 14:14">
            <directory name="Four" size="192" time="Jan 30 14:14">
              <file name="tree.html" size="4779" time="Jan 30 14:15"></file>
              <file name="tree2.html" size="4440" time="Jan 30 14:14"></file>
              <file name="tree4.html" size="4315" time="Jan 30 14:14"></file>
              <file name="tree6.html" size="4190" time="Jan 30 14:14"></file>
            </directory>
            <file name="tree0.html" size="3617" time="Jan 30 14:14"></file>
            <file name="tree1.html" size="3505" time="Jan 30 14:14"></file>
            <file name="tree2.html" size="3393" time="Jan 30 14:14"></file>
            <file name="tree3.html" size="3729" time="Jan 30 14:14"></file>
            <file name="tree4.html" size="3841" time="Jan 30 14:14"></file>
            <file name="tree5.html" size="3953" time="Jan 30 14:14"></file>
            <file name="tree6.html" size="4065" time="Jan 30 14:14"></file>
          </directory>
          <file name="tree2.html" size="3280" time="Jan 30 14:13"></file>
          <file name="tree3.html" size="3182" time="Jan 30 14:13"></file>
        </directory>
        <file name="tree3.html" size="3095" time="Jan 30 14:13"></file>
      </directory>
      <file name="tree3.html" size="3031" time="Jan 30 14:12"></file>
      <file name="tree4.html" size="2957" time="Jan 30 14:12"></file>
    </directory>
    <directory name="Spaces" size="96" time="Jan 30 15:36">
      <directory name="Empty" size="96" time="Jan 30 15:36">
        <directory name="Folder" size="96" time="Jan 30 15:36">
          <directory name="Goes" size="96" time="Jan 30 15:36">
            <directory name="Here" size="64" time="Jan 30 15:36">
            </directory>
          </directory>
        </directory>
      </directory>
    </directory>
    <file name="demo-html.html" size="7803" time="Jan 30 15:40"></file>
    <file name="demo-json.json" size="2962" time="Jan 30 15:40"></file>
    <file name="demo-xml.xml" size="0" time="Jan 30 15:40"></file>
    <file name="tree.html" size="2732" time="Jan 30 14:11"></file>
    <file name="tree2.html" size="2794" time="Jan 30 14:12"></file>
    <file name="tree3.html" size="2855" time="Jan 30 14:12"></file>
    <file name="tree4.html" size="2916" time="Jan 30 14:12"></file>
  </directory>
  <report>
    <directories>10</directories>
    <files>23</files>
  </report>
</tree>
```

## JSON Output
```
tree -hDC -J /Users/macbookpro/acme.sh -o acme.json
```
This will produce the following output in JSON format.

```json
[
  {"type":"directory","name":"/Users/macbookpro/Justin","contents":[
    {"type":"directory","name":"Dirs","size":160,"time":"Jan 30 14:12","contents":[
      {"type":"directory","name":"One","size":128,"time":"Jan 30 14:13","contents":[
        {"type":"directory","name":"Two","size":160,"time":"Jan 30 14:13","contents":[
          {"type":"directory","name":"Three","size":320,"time":"Jan 30 14:14","contents":[
            {"type":"directory","name":"Four","size":192,"time":"Jan 30 14:14","contents":[
              {"type":"file","name":"tree.html","size":4779,"time":"Jan 30 14:15"},
              {"type":"file","name":"tree2.html","size":4440,"time":"Jan 30 14:14"},
              {"type":"file","name":"tree4.html","size":4315,"time":"Jan 30 14:14"},
              {"type":"file","name":"tree6.html","size":4190,"time":"Jan 30 14:14"}
            ]},
            {"type":"file","name":"tree0.html","size":3617,"time":"Jan 30 14:14"},
            {"type":"file","name":"tree1.html","size":3505,"time":"Jan 30 14:14"},
            {"type":"file","name":"tree2.html","size":3393,"time":"Jan 30 14:14"},
            {"type":"file","name":"tree3.html","size":3729,"time":"Jan 30 14:14"},
            {"type":"file","name":"tree4.html","size":3841,"time":"Jan 30 14:14"},
            {"type":"file","name":"tree5.html","size":3953,"time":"Jan 30 14:14"},
            {"type":"file","name":"tree6.html","size":4065,"time":"Jan 30 14:14"}
          ]},
          {"type":"file","name":"tree2.html","size":3280,"time":"Jan 30 14:13"},
          {"type":"file","name":"tree3.html","size":3182,"time":"Jan 30 14:13"}
        ]},
        {"type":"file","name":"tree3.html","size":3095,"time":"Jan 30 14:13"}
      ]},
      {"type":"file","name":"tree3.html","size":3031,"time":"Jan 30 14:12"},
      {"type":"file","name":"tree4.html","size":2957,"time":"Jan 30 14:12"}
    ]},
    {"type":"directory","name":"Spaces","size":96,"time":"Jan 30 15:36","contents":[
      {"type":"directory","name":"Empty","size":96,"time":"Jan 30 15:36","contents":[
        {"type":"directory","name":"Folder","size":96,"time":"Jan 30 15:36","contents":[
          {"type":"directory","name":"Goes","size":96,"time":"Jan 30 15:36","contents":[
            {"type":"directory","name":"Here","size":64,"time":"Jan 30 15:36","contents":[
            ]}
          ]}
        ]}
      ]}
    ]},
    {"type":"file","name":"demo-html.html","size":7803,"time":"Jan 30 15:40"},
    {"type":"file","name":"demo-json.json","size":0,"time":"Jan 30 15:40"},
    {"type":"file","name":"demo-xml.xml","size":2646,"time":"Jan 30 15:40"},
    {"type":"file","name":"tree.html","size":2732,"time":"Jan 30 14:11"},
    {"type":"file","name":"tree2.html","size":2794,"time":"Jan 30 14:12"},
    {"type":"file","name":"tree3.html","size":2855,"time":"Jan 30 14:12"},
    {"type":"file","name":"tree4.html","size":2916,"time":"Jan 30 14:12"}
  ]},
  {"type":"report","directories":10,"files":23}
]
```

## Optional Options
The following options are useful but not necessarily required for the various outputs. I've listed them below so that I don't forget about them or how useful they can be when the time calls for it. 

 * `-a`: Includes hidden files. By default these are hidden.
 * `-f`: Prints the full path prefix. Useful for XML/JSON and not needed for HTML.
 * `-T string`: Replace the default HTML title and H1 header with string.


## Hello

[![Adele - Hello](https://i.snag.gy/N63zuD.jpg)](https://youtu.be/YQHsXMglC9A?t=72 "Adele - Hello")

Thanks for making your way all the way to the bottom. I'm impressed and I thank you. If you'd like, pop me an email to say _hello_. I would love to hear from you. Let me know I am not the only human being left on the plant because I missed my flight playing FIFA 2018.

Justin Hartman  
[Email][2] | [Website][3]








[1]: http://mama.indstate.edu/users/ice/tree/
[2]: mailto:justin@hartman.me?subject=Saying+Hello
[3]: http://justin.hartman.me
