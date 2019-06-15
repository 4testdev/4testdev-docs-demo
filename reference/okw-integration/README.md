# OKW integration

OpenKeyWord \(OKW\) serves as an abstraction layer between the 4Test model and the GUI testing tool, which as of now is only Selenium.

OKW testing instructions are coded with hashtags in choice names.

## Implicit OKW-calls

## Events

### \#started \(app\)

Starts an app.

#### **4Test Example**

```text
GIVEN Chrome IS #started AND URL IS "https://localhost:3000"
```

The resulted OKW is:

```java
EN.StartApp( "Chrome" )
EN.SetValue( "URL", "https://localhost:3000" )
```

The following apps are known by default. These accept know some inputs by default.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Category name</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">
        <p>Known inputs</p>
        <p>(category names)</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Chrome</td>
      <td style="text-align:left">Google Chrome with Selenium webdriver</td>
      <td style="text-align:left">URL</td>
    </tr>
    <tr>
      <td style="text-align:left">Firefox</td>
      <td style="text-align:left">Mozilla Firefox with Selenium webdriver</td>
      <td style="text-align:left">URL</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>You can define your own app

### \#opened \(page\)

Opens a page, or checks if a page is open and activates it.

#### **4Test Example**

```text
WHEN Login IS #opened AND User IS myUser AND Password IS myPassword
```

The resulted OKW is:

```java
EN.SelectWindow( "Login" ) // Login IS #opened
EN.SetValue( "User", "myUser" )
EN.SetValue( "Password", "myPassword" )
```



### \#clicked

Clicks an element

### \#selected

A

### \#typed

Types 

## Attributes

### \#present

### \#label

Checks the label of the element

### \#available

Checks 

### \#visible

Checks if the element is visible



### \#caption \(button/link\)

Checks the caption of GUI-element. The caption is typicaly the visible text of a button,  link or window/dialog.

`#caption` works also together with: `#like` and `#matches` See Matching modes

```text
THEN OK HAS #caption "OK" AND 
 Dialog HAS #caption #like "Error*" AND
 Link HAS #caption #matches "/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/"
```



## Matching modes

### \#like – wildcard match



#### **4Test Example**

```text
THEN User IS #like "*User"
```

The resulted OKW is:

```java
EN.VerifyValueWCM( "User", "*User" )
```

### \#matches – regexp match



#### **4Test Example**

```text
THEN User IS #matches ".*User"
```

The resulted OKW is:

```java
EN.VerifyValueREGX( "User", ".*User" )
```

## Others

### \#and

When multiple elements are selected

