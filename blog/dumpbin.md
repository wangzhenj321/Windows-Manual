## Description

The Microsoft COFF Binary File Dumper (DUMPBIN.EXE) displays information about Common Object File Format (COFF) binary files. You can use DUMPBIN to examine COFF object files, standard libraries of COFF objects, executable files, and dynamic-link libraries (DLLs).

## Synopsis

To run DUMPBIN, use the following syntax:

```
DUMPBIN [options] files...
```

Specify one or more binary files, along with any options required to control the information. DUMPBIN displays the information to standard output. You can either redirect it to a file or use the `/OUT` option to specify a file name for the output.

When you run DUMPBIN on a file without specifying an option, DUMPBIN displays the `/SUMMARY` output.

When you type the command `dumpbin` without any other command-line input, DUMPBIN displays a usage statement that summarizes its options.

## Options

Option names can't be abbreviated. Some options take arguments, specified after a colon (:). No spaces or tabs are allowed within an option specification.

Option names and their keyword or file name arguments aren't case-sensitive. Most options apply to all binary files, but a few apply only to certain types of files. 

- `/DEPENDENTS`

  Dumps the names of the DLLs from which the image imports functions. You can use the list to determine which DLLs to redistribute with your app, or find the name of a missing dependency.

  This option applies to all the executable files specified on the command line. It doesn't take any arguments.

  The `/DEPENDENTS` option adds the names of the DLLs from which the image imports functions to the output. This option does not dump the names of the imported functions. To see the names of the imported functions, use the `/IMPORTS` option.

- `/EXPORTS`

  This option displays all definitions exported from an executable file or DLL.

  <img src="../img/dumpbin/dumpbin-exports.png">
