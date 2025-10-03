# StringCalculator Test Specification

| Test ID | Unit Test Name                          | Input                   | Expected Output / Exception         | Notes (Description)                                 |
|--------|------------------------------------------|-------------------------|-------------------------------------|-----------------------------------------------------|
| TC01   | test_empty_string_returns_zero           | `""`                    | `0`                                 | Returns 0 for empty string input                    |
| TC02   | test_single_number_returns_value         | `"1"`                   | `1`                                 | Returns the number itself for single input          |
| TC03   | test_multiple_numbers_sum                | `"1,2,3,4"`             | `10`                                | Sums unknown amount of numbers                      |
| TC04   | test_newline_delimiter                   | `"1\n2,3"`              | `6`                                 | Supports new line as delimiter                      |
| TC05   | test_newline_only_delimiter              | `"4\n5\n6"`             | `15`                                | Supports only new line as delimiter                 |
| TC06   | test_custom_single_char_delimiter        | `"//;\n1;2"`            | `3`                                 | Supports custom single character delimiter          |
| TC07   | test_custom_single_char_delimiter_alt    | `"//|\n4|5|6"`          | `15`                                | Supports another custom single character delimiter  |
| TC08   | test_custom_multi_char_delimiter         | `"//[***]\n1***2***3"`  | `6`                                 | Supports custom delimiter of any length             |
| TC09   | test_custom_multi_char_delimiter_alt     | `"//[abc]\n2abc3abc4"` | `9`                                 | Supports another custom delimiter of any length     |
| TC10   | test_negative_number_exception           | `"-1,2"`                | Exception: "negatives not allowed: -1" | Throws exception for negative number input      |
| TC11   | test_multiple_negatives_exception        | `"2,-4,3,-5"`           | Exception: "negatives not allowed: -4,-5" | Throws exception listing all negative numbers |
| TC12   | test_ignore_numbers_greater_than_1000    | `"2,1001"`              | `2`                                 | Ignores numbers greater than 1000                   |
| TC13   | test_ignore_numbers_greater_than_1000_alt| `"1000,1001,2"`         | `1002`                              | Ignores numbers greater than 1000                   |
| TC14   | test_cyclomatic_complexity_limit         | N/A                     | N/A                                 | Ensures CCN per function ≤ 3                        |
| TC15   | test_coverage_100_percent                | N/A                     | N/A                                 | Ensures 100% line and branch coverage               |
