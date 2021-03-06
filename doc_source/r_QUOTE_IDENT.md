# QUOTE\_IDENT Function<a name="r_QUOTE_IDENT"></a>

The QUOTE\_IDENT function returns the specified string as a double quoted string so that it can be used as an identifier in a SQL statement\. Appropriately doubles any embedded double quotes\. 

## Syntax<a name="r_QUOTE_IDENT-synopsis"></a>

```
QUOTE_IDENT(string)
```

## Argument<a name="r_QUOTE_IDENT-argument"></a>

 *string*   
The input parameter can be a CHAR or VARCHAR string\. 

## Return Type<a name="r_QUOTE_IDENT-return-type"></a>

The QUOTE\_IDENT function returns the same type string as the input parameter\. 

## Example<a name="r_QUOTE_IDENT-example"></a>

The following example returns the CATNAME column surrounded by quotes: 

```
select catid, quote_ident(catname)
from category
order by 1,2;

 catid | quote_ident
-------+-------------
     1 | "MLB"
     2 | "NHL"
     3 | "NFL"
     4 | "NBA"
     5 | "MLS"
     6 | "Musicals"
     7 | "Plays"
     8 | "Opera"
     9 | "Pop"
    10 | "Jazz"
    11 | "Classical"
(11 rows)
```