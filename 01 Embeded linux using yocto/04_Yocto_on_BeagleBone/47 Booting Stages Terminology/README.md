# Booting Stages Terminology

+--------+----------------+----------------+----------+
| Boot   | Terminology #1 | Terminology #2 | Actual   |
| stage  |                |                | program  |
| number |                |                | name     |
+--------+----------------+----------------+----------+
| 1      |  Primary       |  -             | ROM code |
|        |  Program       |                |          |
|        |  Loader        |                |          |
|        |                |                |          |
| 2      |  Secondary     |  1st stage     | u-boot   |
|        |  Program       |  bootloader    | SPL      |
|        |  Loader (SPL)  |                |          |
|        |                |                |          |
| 3      |  -             |  2nd stage     | u-boot   |
|        |                |  bootloader    |          |
|        |                |                |          |
| 4      |  -             |  -             | kernel   |
|        |                |                |          |
+--------+----------------+----------------+----------+


Reference: https://stackoverflow.com/questions/31244862/what-is-the-use-of-spl-secondary-program-loader
