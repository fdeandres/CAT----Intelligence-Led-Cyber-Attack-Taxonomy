<div class="Box-body readme blob instapaper_body js-code-block-container" id="readme">
    <article class="markdown-body entry-content p-3 p-md-6" itemprop="text"><h1><a aria-hidden="true" class="anchor" href="#t1035---service-execution" id="user-content-t1035---service-execution"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z" fill-rule="evenodd"></path></svg></a>T1035 - Service Execution</h1>
<h2><a aria-hidden="true" class="anchor" href="#description-from-attck" id="user-content-description-from-attck"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z" fill-rule="evenodd"></path></svg></a><a href="https://attack.mitre.org/wiki/Technique/T1035" rel="nofollow">Description from ATT&amp;CK</a></h2>
<blockquote>Adversaries may execute a binary, command, or script via a method that interacts with Windows services, such as the Service Control Manager. This can be done by either creating a new service or modifying an existing service. This technique is the execution used in conjunction with [New Service](<a href="https://attack.mitre.org/techniques/T1050" rel="nofollow">https://attack.mitre.org/techniques/T1050</a>) and [Modify Existing Service](<a href="https://attack.mitre.org/techniques/T1031" rel="nofollow">https://attack.mitre.org/techniques/T1031</a>) during service persistence or privilege escalation.</blockquote>
<h2><a aria-hidden="true" class="anchor" href="#atomic-tests" id="user-content-atomic-tests"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z" fill-rule="evenodd"></path></svg></a>Atomic Tests</h2>
<ul>
<li><a href="#atomic-test-1---execute-a-command-as-a-service">Atomic Test #1 - Execute a Command as a Service</a></li>
</ul>
<br/>
<h2><a aria-hidden="true" class="anchor" href="#atomic-test-1---execute-a-command-as-a-service" id="user-content-atomic-test-1---execute-a-command-as-a-service"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z" fill-rule="evenodd"></path></svg></a>Atomic Test #1 - Execute a Command as a Service</h2>
<p>Creates a service specifying an aribrary command and executes it. When executing commands such as PowerShell, the service will report that it did not start correctly even when code executes properly.</p>
<p><strong>Supported Platforms:</strong> Windows</p>
<h4><a aria-hidden="true" class="anchor" href="#inputs" id="user-content-inputs"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z" fill-rule="evenodd"></path></svg></a>Inputs</h4>
<table>
<thead>
<tr>
<th>Name</th>
<th>Description</th>
<th>Type</th>
<th>Default Value</th>
</tr>
</thead>
<tbody>
<tr>
<td>service_name</td>
<td>Name of service to create</td>
<td>string</td>
<td>ARTService</td>
</tr>
<tr>
<td>executable_command</td>
<td>Command to execute as a service</td>
<td>string</td>
<td>%COMSPEC% /c powershell.exe -nop -w hidden -command New-Item -ItemType File C:�rt-marker.txt</td>
</tr>
</tbody>
</table>
<h4><a aria-hidden="true" class="anchor" href="#run-it-with-command_prompt" id="user-content-run-it-with-command_prompt"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z" fill-rule="evenodd"></path></svg></a>Run it with <code>command_prompt</code>!</h4>
<pre><code>sc.exe create #{service_name} binPath= #{executable_command}
sc.exe start #{service_name}
sc.exe delete #{service_name}
</code></pre>
<br/>
</article>
  </div>