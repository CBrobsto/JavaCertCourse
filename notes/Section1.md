### Referencing a type from another package
* Fully Qualified Class Name (FQCN)
  * `java.util.ArrayList = new java.util.ArrayList();`
* Single-type-import declaration
    *  `import java.util.ArrayList;`
    * Takes precedence of the import-on-demand declaration
    * Will prevent you from creating a class of the same name
* Type-import-on-demand declaration
    * `import java.util.*;`
* Single-static-import declaration
    * `import static java.lang.Math.Pi;`
* Static-import-on-demand declaration
    * `import static java.lang.*;`
    
`java.lang` package is automatically imported. That is why we can use `String` without a FQCN.

An import statement must be the first line of code at the top of the file after the package statement, if a package
statement exists (excluding whitespace and comments).

### Summary
* The package statement is used to group classes into a logical set of classes, that have some commonality.
    * Only one package can be defined in a .java source file.
    * The package statement must be the first line of code (excluding comments and empty lines).
    * No package statement makes the class, or type you define, belong to the unnamed package.
    * To have th compiler create class files in exploded directories, that represent your package names: use `javac -d {directory} foo.java`
    * A class file does NOT have to reside in a directory structure, that represents its package structure

### Low-Hanging Fruit on Exam
* Multiple package statements
* A package statement that is not the first line of code
* Import statement not in the correct order, must be after a package statement if one exists and before any other code
* Import static statement used in place of an import statement
* Import statement using a higher level package with a wild card - `*`, a wild card does not include classes in other packages. 
    * Example: `import a.*` does not also mean `import a.b.*`