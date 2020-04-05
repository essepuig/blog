---
title: "How to create a nice Unit Test template in IntelliJ"
categories:
  - blog
tags:
  - Unit Test
  - Java
  - IntelliJ
  - Developper productivity
---

This is the template I use when working with [IntelliJ Community](https://www.jetbrains.com/idea/) IDE in order to be productive when writting Unit Tests in Junit

To create the template, launch IntelliJ and go to :
```
File -> Settings -> Editor -> Live Templates
```

You should see the following :
![IntelliJ settings]({{ site.url }}{{ site.baseurl }}/assets/images/2020-03-29-intellij-template-for-unit-testing/intelliJ_settings_liveTemplates.png)


Then click the "+" button (on the top right) and choose "Live Template"

The next step is to fill the "Abbreviaton" field (I choose "should" as my favourite abbreviation), set a nice description and paste the following snipped in the "Template text" field:

```java
@org.junit.Test
public void _should_(){

  // Given

  // When
  Object result = null;

  // Then
  org.assertj.core.api.Assertions.assertThat(result).isNotNull();
}
```

Before saving, there is one more step: we need to configure the context where the Live Template can be applied. 

To do so, click on the "Define" link at the bottom of the screen, and the choose "Declaration" under the "Java" list

The complete form should look like :
![IntelliJ settings filled]({{ site.url }}{{ site.baseurl }}/assets/images/2020-03-29-intellij-template-for-unit-testing/intelliJ_settings_liveTemplates_filled.png){: .full}

To save the Live Template, click on the "Apply" button

You can now create a new Junit test by typing "should" and then the IntelliJ autocompletion should propose the new template
