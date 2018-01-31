#### Table of Contents

- [Introduction](#introduction)
- [Tree Options](#tree-options)
- [HTML Output](#html-output)
- [XML Output](#xml-output)
- [JSON Output](#json-output)
- [Optional Options](#optional-options)
- [Credits](#credits)
- [Hello](#hello)

# Introduction
[Tree][1] is a recursive directory listing command that produces a depth indented listing of files, which is colorised ala dircolors if the LS_COLORS environment variable is set and output is to tty. Tree has been ported and reported to work under the following operating systems: Linux, FreeBSD, OS X, Solaris, HP/UX, Cygwin, HP Nonstop and OS/2. 

# Tree Options
Tree has a vast array of options and I've gone through each of them to fine-tune and perfect the outputs for HTML, JSON and XML formats. To see a list of available options simply run `tree --help` from your terminal.

Below is a list of only the options I used to create workable formats for HTML, JSON and XML data formats.

 * `-o filename`: Output to a file instead of stdout.
 * `-h`: Print the size in a more human readable way. Only displays human readable values for the HTML format. JSON and XML objects use raw values for the output.
 * `-D`: Print the date of last modification or (-c) status change.
 * `-C`: Turn colorisation on always.
 * `-X`: Prints out an XML representation of the tree.
 * `-J`: Prints out an JSON representation of the tree.
 * `-H baseHREF`: Prints out HTML format with baseHREF as top directory.

# HTML Output
```zsh
$ tree -hDC -H "/Users/macbookpro/2018-Clients" "/Users/macbookpro/2018-Clients" -o "tree outputs/html-output.html"
```
This will produce the following output in HTML format.

![HTML Output][5]

# XML Output
```zsh
$ tree -hDC -X "/Users/macbookpro/2018-Clients" -o "tree outputs/xml-output.xml"
```
This will produce the following output in XML format.   

```xml
<?xml version="1.0" encoding="UTF-8"?>
<tree>
  <directory name="/Users/macbookpro/2018-Clients">
    <directory name="001. Best Buy" size="256" time="Jan 31  5:46">
      <directory name="Archives" size="192" time="Jan 31  5:44">
        <file name="CI &amp; Brand Templates - 660.zip" size="5598619" time="Jan 31  4:05"></file>
        <file name="Old Website Source Code 1036.zip" size="833619" time="Jan 31  4:05"></file>
        <file name="Old Website Source Code 942.zip" size="1069619" time="Jan 31  4:06"></file>
        <file name="Old Website Source Code 989.zip" size="991619" time="Jan 31  4:06"></file>
      </directory>
      <directory name="Client Status Reports" size="256" time="Jan 31  5:46">
        <file name="Contact Report #1177.docx" size="46106" time="Jan 31  3:59"></file>
        <file name="Contact Report #1318.docx" size="188796" time="Jan 31  4:55"></file>
        <file name="Contact Report #1412.docx" size="228796" time="Jan 31  4:55"></file>
        <file name="Contact Report #1647.docx" size="243796" time="Jan 31  4:56"></file>
        <file name="Contact Report #1788.docx" size="311398" time="Jan 31  4:56"></file>
        <file name="Contact Report #1882.docx" size="204398" time="Jan 31  4:57"></file>
      </directory>
      <directory name="Costings" size="256" time="Jan 31  5:44">
        <file name="Mobile App Development Costing #738.xlsx" size="378398" time="Jan 31  5:16"></file>
        <file name="Mobile App Development Costing #886.xlsx" size="399398" time="Jan 31  5:15"></file>
        <file name="Website Dev Costing #378.xlsx" size="289398" time="Jan 31  5:13"></file>
        <file name="Website Dev Costing #519.xlsx" size="322398" time="Jan 31  5:13"></file>
        <file name="Website Dev Costing #566.xlsx" size="632398" time="Jan 31  5:13"></file>
      </directory>
      <directory name="Financial" size="160" time="Jan 31  5:45">
        <directory name="Invoices" size="192" time="Jan 31  5:45">
          <file name="Invoice #1707.pdf" size="133106" time="Jan 31  4:04"></file>
          <file name="Invoice #2100.pdf" size="89106" time="Jan 31  4:04"></file>
          <file name="Invoice #2493.pdf" size="545106" time="Jan 31  4:03"></file>
          <file name="Invoice #2886.pdf" size="651106" time="Jan 31  4:03"></file>
        </directory>
        <directory name="Work Orders" size="224" time="Jan 31  5:45">
          <file name="Work Order #1353.pdf" size="61106" time="Jan 31  4:02"></file>
          <file name="Work Order #1589.pdf" size="59106" time="Jan 31  4:02"></file>
          <file name="Work Order #645.pdf" size="300106" time="Jan 31  4:03"></file>
          <file name="Work Order #763.pdf" size="204106" time="Jan 31  4:02"></file>
          <file name="Work Order #999.pdf" size="29106" time="Jan 31  4:02"></file>
        </directory>
      </directory>
      <directory name="Images &amp; Layouts" size="192" time="Jan 31  5:45">
        <file name="website-homepage-00101.jpg" size="54106" time="Jan 31  4:01"></file>
        <file name="website-homepage-06920.jpg" size="333106" time="Jan 31  4:01"></file>
        <file name="website-homepage-09193.jpg" size="199106" time="Jan 31  4:01"></file>
        <file name="website-homepage-16012.jpg" size="489106" time="Jan 31  4:00"></file>
      </directory>
    </directory>
    <directory name="002. Walmart" size="256" time="Jan 31  5:43">
      <directory name="Archives" size="160" time="Jan 31  5:46">
        <file name="CI &amp; Brand Templates - 707.zip" size="471619" time="Jan 31  4:05"></file>
        <file name="Old Website Source Code 1083.zip" size="79619" time="Jan 31  4:05"></file>
        <file name="Old Website Source Code 1130.zip" size="671619" time="Jan 31  4:05"></file>
      </directory>
      <directory name="Costings" size="224" time="Jan 31  5:47">
        <file name="Mobile App Development Costing #775.xlsx" size="649398" time="Jan 31  5:16"></file>
        <file name="Website Dev Costing #425.xlsx" size="556398" time="Jan 31  5:13"></file>
        <file name="Website Dev Costing #472.xlsx" size="501398" time="Jan 31  5:13"></file>
        <file name="Website Dev Costing #613.xlsx" size="400398" time="Jan 31  5:14"></file>
      </directory>
      <directory name="Financial" size="160" time="Jan 31  5:47">
        <directory name="Invoices" size="256" time="Jan 31  5:49">
          <file name="Invoice #1838.pdf" size="1222106" time="Jan 31  4:04"></file>
          <file name="Invoice #1969.pdf" size="901106" time="Jan 31  4:04"></file>
          <file name="Invoice #2231.pdf" size="795106" time="Jan 31  4:04"></file>
          <file name="Invoice #2362.pdf" size="666106" time="Jan 31  4:03"></file>
          <file name="Invoice #2624.pdf" size="487106" time="Jan 31  4:03"></file>
          <file name="Invoice #2755.pdf" size="344106" time="Jan 31  4:03"></file>
        </directory>
        <directory name="Work Orders" size="288" time="Jan 31  5:49">
          <file name="Work Order #1117.pdf" size="83106" time="Jan 31  4:02"></file>
          <file name="Work Order #1235.pdf" size="99106" time="Jan 31  4:02"></file>
          <file name="Work Order #1471.pdf" size="667106" time="Jan 31  4:02"></file>
          <file name="Work Order #291.pdf" size="100106" time="Jan 31  4:03"></file>
          <file name="Work Order #409.pdf" size="67106" time="Jan 31  4:03"></file>
          <file name="Work Order #527.pdf" size="215106" time="Jan 31  4:03"></file>
          <file name="Work Order #881.pdf" size="126106" time="Jan 31  4:02"></file>
        </directory>
      </directory>
      <directory name="Images &amp; Layouts" size="256" time="Jan 31  5:51">
        <file name="website-homepage-02374.jpg" size="673106" time="Jan 31  4:01"></file>
        <file name="website-homepage-04647.jpg" size="200106" time="Jan 31  4:01"></file>
        <file name="website-homepage-11466.jpg" size="738106" time="Jan 31  4:01"></file>
        <file name="website-homepage-13739.jpg" size="322106" time="Jan 31  4:01"></file>
        <file name="website-homepage-18285.jpg" size="516106" time="Jan 31  4:00"></file>
      </directory>
      <directory name="Status Reports" size="384" time="Jan 31  5:52">
        <file name="Contact Report #1224.docx" size="136596" time="Jan 31  4:54"></file>
        <file name="Contact Report #1271.docx" size="291596" time="Jan 31  4:54"></file>
        <file name="Contact Report #1365.docx" size="385796" time="Jan 31  4:55"></file>
        <file name="Contact Report #1459.docx" size="301796" time="Jan 31  4:55"></file>
        <file name="Contact Report #1506.docx" size="299796" time="Jan 31  4:55"></file>
        <file name="Contact Report #1553.docx" size="100796" time="Jan 31  4:55"></file>
        <file name="Contact Report #1600.docx" size="533796" time="Jan 31  4:56"></file>
        <file name="Contact Report #1694.docx" size="441796" time="Jan 31  4:56"></file>
        <file name="Contact Report #1741.docx" size="441398" time="Jan 31  4:56"></file>
        <file name="Contact Report #1835.docx" size="199398" time="Jan 31  4:57"></file>
      </directory>
    </directory>
    <directory name="_client_backups" size="384" time="Jan 31  5:40">
      <file name="GKDWxAA39CKM.bin" size="24576" time="Jan 31  3:58"></file>
      <file name="OMK8KLcft5nd.bin" size="544768" time="Jan 31  3:57"></file>
      <file name="PG6WP9navcNe.bin" size="544768" time="Jan 31  3:57"></file>
      <file name="RVVPdZpgSwlU.bin" size="544768" time="Jan 31  3:56"></file>
      <file name="S78A6STfNPVd.bin" size="544768" time="Jan 31  3:57"></file>
      <file name="kmAzwMJmKsyw.bin" size="544768" time="Jan 31  3:56"></file>
      <file name="sYpV2IwryDw8.bin" size="24576" time="Jan 31  3:58"></file>
      <file name="wEWVz6Mt61Le.bin" size="24576" time="Jan 31  3:58"></file>
      <file name="xaFc3vEWF28O.bin" size="24576" time="Jan 31  3:58"></file>
    </directory>
    <directory name="tree outputs" size="160" time="Jan 31  7:45">
      <file name="html-output.html" size="21931" time="Jan 31  7:58"></file>
      <file name="xml-output.xml" size="0" time="Jan 31  7:59"></file>
    </directory>
  </directory>
  <report>
    <directories>18</directories>
    <files>74</files>
  </report>
</tree>
```

# JSON Output
```zsh
$ tree -DC -J "/Users/macbookpro/2018-Clients" -o "tree outputs/json-output.json"
```
This will produce the following output in JSON format.

```json
[
  {"type":"directory","name":"/Users/macbookpro/2018-Clients","contents":[
    {"type":"directory","name":"001. Best Buy","size":256,"time":"Jan 31  5:46","contents":[
      {"type":"directory","name":"Archives","size":192,"time":"Jan 31  5:44","contents":[
        {"type":"file","name":"CI &amp; Brand Templates - 660.zip","size":5598619,"time":"Jan 31  4:05"},
        {"type":"file","name":"Old Website Source Code 1036.zip","size":833619,"time":"Jan 31  4:05"},
        {"type":"file","name":"Old Website Source Code 942.zip","size":1069619,"time":"Jan 31  4:06"},
        {"type":"file","name":"Old Website Source Code 989.zip","size":991619,"time":"Jan 31  4:06"}
      ]},
      {"type":"directory","name":"Client Status Reports","size":256,"time":"Jan 31  5:46","contents":[
        {"type":"file","name":"Contact Report #1177.docx","size":46106,"time":"Jan 31  3:59"},
        {"type":"file","name":"Contact Report #1318.docx","size":188796,"time":"Jan 31  4:55"},
        {"type":"file","name":"Contact Report #1412.docx","size":228796,"time":"Jan 31  4:55"},
        {"type":"file","name":"Contact Report #1647.docx","size":243796,"time":"Jan 31  4:56"},
        {"type":"file","name":"Contact Report #1788.docx","size":311398,"time":"Jan 31  4:56"},
        {"type":"file","name":"Contact Report #1882.docx","size":204398,"time":"Jan 31  4:57"}
      ]},
      {"type":"directory","name":"Costings","size":256,"time":"Jan 31  5:44","contents":[
        {"type":"file","name":"Mobile App Development Costing #738.xlsx","size":378398,"time":"Jan 31  5:16"},
        {"type":"file","name":"Mobile App Development Costing #886.xlsx","size":399398,"time":"Jan 31  5:15"},
        {"type":"file","name":"Website Dev Costing #378.xlsx","size":289398,"time":"Jan 31  5:13"},
        {"type":"file","name":"Website Dev Costing #519.xlsx","size":322398,"time":"Jan 31  5:13"},
        {"type":"file","name":"Website Dev Costing #566.xlsx","size":632398,"time":"Jan 31  5:13"}
      ]},
      {"type":"directory","name":"Financial","size":160,"time":"Jan 31  5:45","contents":[
        {"type":"directory","name":"Invoices","size":192,"time":"Jan 31  5:45","contents":[
          {"type":"file","name":"Invoice #1707.pdf","size":133106,"time":"Jan 31  4:04"},
          {"type":"file","name":"Invoice #2100.pdf","size":89106,"time":"Jan 31  4:04"},
          {"type":"file","name":"Invoice #2493.pdf","size":545106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Invoice #2886.pdf","size":651106,"time":"Jan 31  4:03"}
        ]},
        {"type":"directory","name":"Work Orders","size":224,"time":"Jan 31  5:45","contents":[
          {"type":"file","name":"Work Order #1353.pdf","size":61106,"time":"Jan 31  4:02"},
          {"type":"file","name":"Work Order #1589.pdf","size":59106,"time":"Jan 31  4:02"},
          {"type":"file","name":"Work Order #645.pdf","size":300106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Work Order #763.pdf","size":204106,"time":"Jan 31  4:02"},
          {"type":"file","name":"Work Order #999.pdf","size":29106,"time":"Jan 31  4:02"}
        ]}
      ]},
      {"type":"directory","name":"Images &amp; Layouts","size":192,"time":"Jan 31  5:45","contents":[
        {"type":"file","name":"website-homepage-00101.jpg","size":54106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-06920.jpg","size":333106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-09193.jpg","size":199106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-16012.jpg","size":489106,"time":"Jan 31  4:00"}
      ]}
    ]},
    {"type":"directory","name":"002. Walmart","size":256,"time":"Jan 31  5:43","contents":[
      {"type":"directory","name":"Archives","size":160,"time":"Jan 31  5:46","contents":[
        {"type":"file","name":"CI &amp; Brand Templates - 707.zip","size":471619,"time":"Jan 31  4:05"},
        {"type":"file","name":"Old Website Source Code 1083.zip","size":79619,"time":"Jan 31  4:05"},
        {"type":"file","name":"Old Website Source Code 1130.zip","size":671619,"time":"Jan 31  4:05"}
      ]},
      {"type":"directory","name":"Costings","size":224,"time":"Jan 31  5:47","contents":[
        {"type":"file","name":"Mobile App Development Costing #775.xlsx","size":649398,"time":"Jan 31  5:16"},
        {"type":"file","name":"Website Dev Costing #425.xlsx","size":556398,"time":"Jan 31  5:13"},
        {"type":"file","name":"Website Dev Costing #472.xlsx","size":501398,"time":"Jan 31  5:13"},
        {"type":"file","name":"Website Dev Costing #613.xlsx","size":400398,"time":"Jan 31  5:14"}
      ]},
      {"type":"directory","name":"Financial","size":160,"time":"Jan 31  5:47","contents":[
        {"type":"directory","name":"Invoices","size":256,"time":"Jan 31  5:49","contents":[
          {"type":"file","name":"Invoice #1838.pdf","size":1222106,"time":"Jan 31  4:04"},
          {"type":"file","name":"Invoice #1969.pdf","size":901106,"time":"Jan 31  4:04"},
          {"type":"file","name":"Invoice #2231.pdf","size":795106,"time":"Jan 31  4:04"},
          {"type":"file","name":"Invoice #2362.pdf","size":666106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Invoice #2624.pdf","size":487106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Invoice #2755.pdf","size":344106,"time":"Jan 31  4:03"}
        ]},
        {"type":"directory","name":"Work Orders","size":288,"time":"Jan 31  5:49","contents":[
          {"type":"file","name":"Work Order #1117.pdf","size":83106,"time":"Jan 31  4:02"},
          {"type":"file","name":"Work Order #1235.pdf","size":99106,"time":"Jan 31  4:02"},
          {"type":"file","name":"Work Order #1471.pdf","size":667106,"time":"Jan 31  4:02"},
          {"type":"file","name":"Work Order #291.pdf","size":100106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Work Order #409.pdf","size":67106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Work Order #527.pdf","size":215106,"time":"Jan 31  4:03"},
          {"type":"file","name":"Work Order #881.pdf","size":126106,"time":"Jan 31  4:02"}
        ]}
      ]},
      {"type":"directory","name":"Images &amp; Layouts","size":256,"time":"Jan 31  5:51","contents":[
        {"type":"file","name":"website-homepage-02374.jpg","size":673106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-04647.jpg","size":200106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-11466.jpg","size":738106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-13739.jpg","size":322106,"time":"Jan 31  4:01"},
        {"type":"file","name":"website-homepage-18285.jpg","size":516106,"time":"Jan 31  4:00"}
      ]},
      {"type":"directory","name":"Status Reports","size":384,"time":"Jan 31  5:52","contents":[
        {"type":"file","name":"Contact Report #1224.docx","size":136596,"time":"Jan 31  4:54"},
        {"type":"file","name":"Contact Report #1271.docx","size":291596,"time":"Jan 31  4:54"},
        {"type":"file","name":"Contact Report #1365.docx","size":385796,"time":"Jan 31  4:55"},
        {"type":"file","name":"Contact Report #1459.docx","size":301796,"time":"Jan 31  4:55"},
        {"type":"file","name":"Contact Report #1506.docx","size":299796,"time":"Jan 31  4:55"},
        {"type":"file","name":"Contact Report #1553.docx","size":100796,"time":"Jan 31  4:55"},
        {"type":"file","name":"Contact Report #1600.docx","size":533796,"time":"Jan 31  4:56"},
        {"type":"file","name":"Contact Report #1694.docx","size":441796,"time":"Jan 31  4:56"},
        {"type":"file","name":"Contact Report #1741.docx","size":441398,"time":"Jan 31  4:56"},
        {"type":"file","name":"Contact Report #1835.docx","size":199398,"time":"Jan 31  4:57"}
      ]}
    ]},
    {"type":"directory","name":"_client_backups","size":384,"time":"Jan 31  5:40","contents":[
      {"type":"file","name":"GKDWxAA39CKM.bin","size":24576,"time":"Jan 31  3:58"},
      {"type":"file","name":"OMK8KLcft5nd.bin","size":544768,"time":"Jan 31  3:57"},
      {"type":"file","name":"PG6WP9navcNe.bin","size":544768,"time":"Jan 31  3:57"},
      {"type":"file","name":"RVVPdZpgSwlU.bin","size":544768,"time":"Jan 31  3:56"},
      {"type":"file","name":"S78A6STfNPVd.bin","size":544768,"time":"Jan 31  3:57"},
      {"type":"file","name":"kmAzwMJmKsyw.bin","size":544768,"time":"Jan 31  3:56"},
      {"type":"file","name":"sYpV2IwryDw8.bin","size":24576,"time":"Jan 31  3:58"},
      {"type":"file","name":"wEWVz6Mt61Le.bin","size":24576,"time":"Jan 31  3:58"},
      {"type":"file","name":"xaFc3vEWF28O.bin","size":24576,"time":"Jan 31  3:58"}
    ]},
    {"type":"directory","name":"tree outputs","size":192,"time":"Jan 31  8:02","contents":[
      {"type":"file","name":"html-output.html","size":22113,"time":"Jan 31  8:00"},
      {"type":"file","name":"json-output.json","size":0,"time":"Jan 31  8:02"},
      {"type":"file","name":"xml-output.xml","size":8255,"time":"Jan 31  7:59"}
    ]}
  ]},
  {"type":"report","directories":18,"files":75}
]
```

# Optional Options
The following options are useful but not necessarily required for the various outputs. I've listed them below so that I don't forget about them or how useful they can be when the time calls for it. 

 * `-a`: Includes hidden files. By default these are hidden.
 * `-f`: Prints the full path prefix. Useful for XML/JSON and not needed for HTML.
 * `-T string`: Replace the default HTML title and H1 header with string.

# Credits
The following resources helped me put this all together.

 * [tree v1.7.0][1] by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro.
 * [Fake File Generator][4]: a brilliant resource that allows you to create files that can vary in size, extension and naming yet contain no data. This was used to put the directory tree together and to allow me to upload these files so that you can play around with `tree` as well.

# Hello

[![Adele - Hello][6]][7]

Thanks for making your way all the way to the bottom. I'm impressed and I thank you. If you'd like, [pop me an email][2] to say _hello_. I would love to hear from you. Let me know I am not the only human being left on the planet because I missed my flight playing FIFA 2018. :-)

Justin Hartman  
[Email][2] | [Website][3]












[1]: http://mama.indstate.edu/users/ice/tree/
[2]: mailto:justin@hartman.me?subject=Saying+Hello
[3]: http://justin.hartman.me
[4]: http://www.fakefilegenerator.com
[5]: https://i.snag.gy/a6WKU5.jpg
[6]: https://i.snag.gy/N63zuD.jpg
[7]: https://youtu.be/YQHsXMglC9A?t=72
