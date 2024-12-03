国内经常使用Docker的朋友，可能都会涉及到配置镜像源的操作，来加速自己的镜像拉取。然而这段时间陆续发现曾经常用的国内镜像站（各种云商和高校镜像站）现在已经不能用了，搜索互联网可用镜像站或者镜像加速地址，并测试后汇总如下，使用前请自行斟酌。
<h1 id="docker-镜像加速列表截止到20241010">Docker 镜像加速列表</h1>
注意有些镜像站仅包含基础镜像或白名单镜像，如果一个加速地址拉不到需要的镜像，可切换其他地址尝试，当然如果侵犯的您的权益，请联系我删除~
<div class="table-wrapper">
<table style="width: 43.5747%;">
<thead>
<tr>
<th style="width: 72.6236%;">DockerHub 镜像仓库</th>
<th style="width: 67.3004%;">是否正常</th>
</tr>
</thead>
<tbody>
<tr>
<td style="width: 72.6236%;">docker.registry.cyou</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker-cf.registry.cyou</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">dockerpull.com</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">dockerproxy.cn</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.1panel.live</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.rat.dev</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">dhub.kubesre.xyz</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.hlyun.org</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.kejilion.pro</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">registry.dockermirror.com</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.mrxn.net</td>
<td style="width: 67.3004%;">失效</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.chenby.cn</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">ccr.ccs.tencentyun.com</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.littlediary.cn</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.firefly.store</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.nat.tf</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.yuzuha.cc</td>
<td style="width: 67.3004%;">失效</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.crdz.gq</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">noohub.ru</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.nastool.de</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.docker-ttc.xyz</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">freeno.xyz</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.hpcloud.cloud</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">dislabaiot.xyz</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">docker.wget.at</td>
<td style="width: 67.3004%;">失效</td>
</tr>
<tr>
<td style="width: 72.6236%;">ginger20240704.asia</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">lynn520.xyz</td>
<td style="width: 67.3004%;">失效</td>
</tr>
<tr>
<td style="width: 72.6236%;">doublezonline.cloud</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">dockerproxy.com</td>
<td style="width: 67.3004%;">正常</td>
</tr>
<tr>
<td style="width: 72.6236%;">hub.xdark.top</td>
<td style="width: 67.3004%;">新增</td>
</tr>
</tbody>
</table>
</div>
<h2 id="配置方式1临时使用">配置方式1：临时使用</h2>
直接使用，直接拿镜像域名拼接上官方镜像名，例如要拉去镜像yidadaa/chatgpt-next-web，可以用下面写法（不要带 https://）
<pre class="highlighter-hljs"><code class="highlighter-hljs hljs language-bash"> docker pull dockerpull.com/yidadaa/chatgpt-next-web
</code></pre>
<h2 id="配置方式2长久有效">配置方式2：长久有效</h2>
Ubuntu 16.04+、Debian 8+、CentOS 7+

修改文件 /etc/docker/daemon.json（如果不存在则需要创建创建，注意不要写入中文），并重启服务。
<pre class="highlighter-hljs"><code class="highlighter-hljs hljs language-bash">sudo <span class="hljs-built_in">mkdir</span> -p /etc/docker
sudo <span class="hljs-built_in">tee</span> /etc/docker/daemon.json &lt;&lt;-<span class="hljs-string">'EOF'</span>
{
    <span class="hljs-string">"registry-mirrors"</span>: [
    	<span class="hljs-string">"https://dockerpull.com"</span>,
        <span class="hljs-string">"https://docker.anyhub.us.kg"</span>,
        <span class="hljs-string">"https://dockerhub.jobcher.com"</span>,
        <span class="hljs-string">"https://dockerhub.icu"</span>,
        <span class="hljs-string">"https://docker.awsl9527.cn"</span>
    ]
}
EOF
sudo systemctl daemon-reload &amp;&amp; sudo systemctl restart docker
</code></pre>
可直接使用docker pull拉去镜像进行测试，或用以下命令检查是否生效：
<pre class="highlighter-hljs"><code class="highlighter-hljs hljs language-armasm"><span class="hljs-symbol">docker</span> <span class="hljs-meta">info</span></code></pre>