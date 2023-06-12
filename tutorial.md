# Regex Tutorial: Email Validation

## Introduction
Welcome to this tutorial on email validation using regular expressions (regex). In this tutorial, we will explore how to construct a regex pattern for validating email addresses. We will break down the components of the regex and explain their purpose, providing examples along the way.

## Table of Contents:
- [Regex Tutorial: Email Validation](#regex-tutorial-email-validation)
  - [Introduction](#introduction)
  - [Table of Contents:](#table-of-contents)
  - [Regex Summary](#regex-summary)
  - [Component Breakdown](#component-breakdown)
    - [1. Username](#1-username)
    - [2. @ Symbol](#2--symbol)
    - [3. Domain Name](#3-domain-name)
    - [4. Top-Level Domain (TLD)](#4-top-level-domain-tld)
  - [Author](#author)
  - [Conclusion](#conclusion)

## Regex Summary
The regex pattern for email validation is:
```md
/^[a-zA-Z0-9]+([._-][a-zA-Z0-9]+)*@[a-zA-Z0-9]+([.-][a-zA-Z0-9]+)*\.[a-zA-Z]{2,}$/i
```
Now let's dive into each component of this pattern to understand its function.

## Component Breakdown

### 1. Username
The username part of an email address consists of alphanumeric characters and certain special characters like dots (.), underscores (_), and hyphens (-). It cannot start or end with a dot, and consecutive dots are not allowed.
```md
^[a-zA-Z0-9]+([._-][a-zA-Z0-9]+)*
```
- ^[a-zA-Z0-9]+ matches one or more alphanumeric characters at the beginning of the string.
- ([._-][a-zA-Z0-9]+)* allows for the presence of dots, underscores, or hyphens followed by alphanumeric characters, and this group can repeat zero or more times.
- Example: max.keable


### 2. @ Symbol
The @ symbol separates the username from the domain name in an email address.
```md
@
```
Example: @


### 3. Domain Name
The domain name part of an email address consists of alphanumeric characters, dots, and hyphens, separated by dots. It must have at least one dot.
```md
[a-zA-Z0-9]+([.-][a-zA-Z0-9]+)*
```
- [a-zA-Z0-9]+ matches one or more alphanumeric characters at the beginning of the domain name.
- ([.-][a-zA-Z0-9]+)* allows for the presence of dots or hyphens followed by alphanumeric characters, and this group can repeat zero or more times.
- Example: example.com


### 4. Top-Level Domain (TLD)
The top-level domain represents the domain's type, such as .com, .org, or .net. It consists of a dot followed by two or more alphabetic characters.
```md 
\.[a-zA-Z]{2,}$
```
- \. matches a dot character.
- [a-zA-Z]{2,} matches two or more alphabetic characters.
- Example: .com

## Author 

This tutorial was created by [MaxKeable](https://github.com/MaxKeable) You can find more projects and tutorials on [My GitHub](https://github.com/MaxKeable).

Congratulations! You now have a solid understanding of how to use regex for email validation. Remember to adapt the regex pattern to your specific requirements and consider additional validation steps if necessary.

## Conclusion
In this tutorial, we explored how to construct a regex pattern for email validation. We examined each component of the pattern, including the username, @ symbol, domain name, and top-level domain. Each component plays a crucial role in validating an email address.

Now you can confidently utilize regex to validate email addresses in your web development projects. Enjoy applying your newfound knowledge!

If you have any further questions, feel free to reach out!