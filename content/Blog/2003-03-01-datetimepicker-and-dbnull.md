<p class="MsoNormal" style="MARGIN: 0in 0in 0pt">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><br /> <font face="Trebuchet MS"><br /> <font color="teal">You can’t bind a Windows Forms DateTimePicker to a field<br /> that might contain DBNull… so I did this;<o:p></o:p></font><br /> </font><br /> </span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><o:p>&nbsp;</o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span style="COLOR: blue">public</span> <span style="COLOR: blue">class</span><br /> DBDateTimePicker:DateTimePicker<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>{<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><o:p>&nbsp;</o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 2">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">public</span><br /> DBDateTimePicker()<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 2">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>{<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 3">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: green">//<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 3">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: green">// TODO: Add constructor logic<br /> here<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 3">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: green">//<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 2">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>}<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><o:p>&nbsp;</o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">public</span> <span style="COLOR: blue">object</span> DBValue<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>{<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">get<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>{<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">if</span> (<span style="COLOR: blue">this</span>.Checked)<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">return</span> <span style="COLOR: blue">base</span>.Value;<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">else<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">return</span><br /> System.DBNull.Value;<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>}<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">set<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>{<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">if</span> (System.Convert.IsDBNull(<span style="COLOR: blue">value</span>))<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </span><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span style="COLOR: blue">this</span>.Checked=<span style="COLOR: blue">false</span>;<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">else<o:p></o:p></span></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span><span style="COLOR: blue">this</span>.Value = Convert.ToDateTime(<span style="COLOR: blue">value</span>);<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>}<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>}<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt; mso-layout-grid-align: none">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: 'Courier New'"><span style="mso-tab-count: 1">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br /> </span>}<o:p></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><o:p>&nbsp;</o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><font face="Trebuchet MS" color="teal">Then I bind to “DBValue”&nbsp; (instead of Value) and it appears to<br /> work fine… if it is null, it is unchecked and disabled, otherwise it is enabled<br /> and can be set to any normal date value&#8230; if you uncheck the box yourself, then<br /> the data field&nbsp;is set to DBNull&#8230;</font></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><o:p><font face="Trebuchet MS" color="teal">&nbsp;</font></o:p></span>
</p>

<p class="MsoNormal" style="MARGIN: 0in 0in 0pt">
  <span style="FONT-SIZE: 10pt; FONT-FAMILY: Arial"><font face="Trebuchet MS" color="teal">Not sure if it the best idea, but I can’t override Value so this<br /> seems like a reasonable alternative… of course, I never looked around for the<br /> &#8220;official&#8221; solution or any other possible answers, so let me know if you have a<br /> better idea!</font></span>
</p>