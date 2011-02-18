### About:

Copy files to and from a remote host using sftp. Based on phing scp task.

### Usage:

     <taskdef name="sftp" classname="path.to.task.SftpTask" />

     <sftp username="john" password="secret" host="example.com" todir="/public_html" file="index.html" />

     <sftp username="john" password="secret" host="example.com" todir="/public_html/app">
        <fileset dir="template">
            <include name="*.html" />
        </fileset>
     </sftp>

#### Attributes

<table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Type</th>
          <th>Description</th>
          <th>Default</th>
          <th>Required</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>host</td>
          <td>String</td>
          <td>Remote host</td>
          <td>none</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>port</td>
          <td>Integer</td>
          <td>Remote port</td>
          <td>22</td>
          <td>No</td>
        </tr>
        <tr>
          <td>username</td>
          <td>String</td>
          <td>Username to use for the connection</td>
          <td>none</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>password</td>
          <td>String</td>
          <td>Password to use for the connection</td>
          <td>none</td>
          <td>No</td>
        </tr>
        <tr>
          <td>autocreate</td>
          <td>Boolean</td>
          <td>Whether to autocreate remote directories</td>
          <td>true</td>
          <td>No</td>
        </tr>
        <tr>
          <td>todir</td>
          <td>String</td>
          <td>Directory to put file(s) in</td>
          <td>none</td>
          <td>No</td>
        </tr>
        <tr>
          <td>file</td>
          <td>String</td>
          <td>Filename to use</td>
          <td>none</td>
          <td>No</td>
        </tr>
        <tr>
          <td>fetch</td>
          <td>Boolean</td>
          <td>Whether to fetch (instead of copy to) the file</td>
          <td>false</td>
          <td>No</td>
        </tr>
      </tbody>
    </table>
