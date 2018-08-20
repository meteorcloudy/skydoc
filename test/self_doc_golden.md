<a name="#skydoc"></a>
## skydoc

<pre>
skydoc(name, deps, out, rule_names, skydoc, target_file)
</pre>


Generates documentation for exported skylark rule definitions in a target skylark file.

This rule is an experimental replacement for the existing skylark_doc rule. It generates
documentation for rule definitions in a target .bzl file.


### Attributes

<table class="params-table">
  <colgroup>
    <col class="col-param" />
    <col class="col-description" />
  </colgroup>
  <tbody>
    <tr id="#skydoc_name">
      <td><code>name</code></td>
      <td>
        String; required
        <p>
          A unique name for this rule.
        </p>
      </td>
    </tr>
    <tr id="#skydoc_deps">
      <td><code>deps</code></td>
      <td>
        List of labels; optional
        <p>
          A list of skylark_library dependencies which target_file depends on.
        </p>
      </td>
    </tr>
    <tr id="#skydoc_out">
      <td><code>out</code></td>
      <td>
        Label; required
        <p>
          The file to which documentation will be output.
        </p>
      </td>
    </tr>
    <tr id="#skydoc_rule_names">
      <td><code>rule_names</code></td>
      <td>
        List of strings; optional
        <p>
          A list of rule names to generate documentation for. These should correspond to
the names of exported symbols for rule definitions in the target file. If this list
is empty, then documentation for all exported rule definitions will be generated.
        </p>
      </td>
    </tr>
    <tr id="#skydoc_skydoc">
      <td><code>skydoc</code></td>
      <td>
        Label; optional
        <p>
          The location of the skydoc tool.
        </p>
      </td>
    </tr>
    <tr id="#skydoc_target_file">
      <td><code>target_file</code></td>
      <td>
        Label; optional
        <p>
          The skylark file to generate documentation for.
        </p>
      </td>
    </tr>
  </tbody>
</table>


