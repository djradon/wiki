
## Implementation

- uses [[prdct.Postgres]], keeps triples in one big table.

Complex Data Type 
PostgreSQL provides a list of primitive data types, such as numeric, monetary, character, binary, date and time, boolean, etc. PostgreSQL also provides a way to define new data types by the CREATE TYPE statement. To implement BiTRDF, we first create a complex data type, named BiTemporalResource. The statement [115] for creating BiTemporalResource is as follows: 

CREATE TYPE BiTemporalResource AS (
  Name VARCHAR ,
  VtBegin TIMESTAMP WITH TIME ZONE ,
  VtEnd TIMESTAMP WITH TIME ZONE ,
  TtBegin TIMESTAMP WITH TIME ZONE ,
  TtEnd TIMESTAMP WITH TIME ZONE ,
);

## References

-  [BiTRDF: Extending RDF for BiTemporal Data](https://academicworks.cuny.edu/cgi/viewcontent.cgi?article=6041&context=gc_etds)