public int indexOf(int ch,
          int fromIndex)
Returns the index within this string of the first occurrence of the specified character, starting the search at the specified index.
If a character with value ch occurs in the character sequence represented by this String object at an index no smaller than fromIndex, then the index of the first such occurrence is returned. For values of ch in the range from 0 to 0xFFFF (inclusive), this is the smallest value k such that:

 (this.charAt(k) == ch) && (k >= fromIndex)
 
is true. For other values of ch, it is the smallest value k such that:
 (this.codePointAt(k) == ch) && (k >= fromIndex)
 
is true. In either case, if no such character occurs in this string at or after position fromIndex, then -1 is returned.
There is no restriction on the value of fromIndex. If it is negative, it has the same effect as if it were zero: this entire string may be searched. If it is greater than the length of this string, it has the same effect as if it were equal to the length of this string: -1 is returned.

All indices are specified in char values (Unicode code units).

Parameters:
ch - a character (Unicode code point).
fromIndex - the index to start the search from.
Returns:
the index of the first occurrence of the character in the character sequence represented by this object that is greater than or equal to fromIndex, or -1 if the character does not occur.

public int indexOf(String str,
          int fromIndex)
Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.
The returned index is the smallest value k for which:

 k >= fromIndex && this.startsWith(str, k)
 
If no such value of k exists, then -1 is returned.
Parameters:
str - the substring to search for.
fromIndex - the index from which to start the search.
Returns:
the index of the first occurrence of the specified substring, starting at the specified index, or -1 if there is no such occurrence.

findKeyword("She's my sister", "sister", 0);

Iteration       psn        before       after
 1              9            " "         NA

 findKeyword("Brother Tom is helpful", "brother",0);

 Iteration       psn        before       after
 1                           NA           " "


 findKeyword("I can't catch wild cats.", "cat", 0);
 Iteration       psn        before       after
 1                 8          " "         "c"
 2                  19         " "        "s"

 findKeyword("I know nothing about snow plows.", "no", 0);

Iteration       psn        before       after
 1               3          "k"         "w"
 2               7          " "         "t"
 3               22         "s"         "w"

  Statement: I want to build a robot 
  Response: What would it mean to build a robot? 

  Statement: I want to understand French. 
  Response: What would it mean to understand French? 

  Statement: Do you like me?
Response: What makes you think that I like you?

Statement: You confuse me
Response: What makes you think that I confuse you?