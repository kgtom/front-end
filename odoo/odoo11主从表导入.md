---


---

<h2 id="重点">重点</h2>
<ol>
<li>
<p><strong>这里的难点是从表涉及到外键的问题。</strong></p>
<p><strong>注意这里的id字段，这里不再是单纯的int类型的字段，而是’<strong>export</strong>.table_’+id+'<em>1’的格式，即__export</em>_.{odoo Model类名称}_{id序列号}。</strong></p>
<p><strong>其他字段和类的字段名称相同即可。</strong></p>
</li>
<li>
<p><strong>第二点就是外键的问题，这个基本上是我们处理问题的核心处，命名的格式是{odoo主表对应的类名称}_id/id,我们的主表名为table,所以结果是table_id/id;</strong></p>
<p><strong>内容格式是’<strong>export</strong>.{odoo Model主表表类名称}_{序列号}’，这里是主表，即表示外键，结果是__export__.table_具体id值.</strong></p>
</li>
</ol>
<blockquote>
<p>reference:<a href="https://www.cnblogs.com/crazyguo/p/8534679.html">addr</a></p>
</blockquote>

