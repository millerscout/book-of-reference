//implicit conversion

``` CSharp
var paramvalue = "t";

using (var con = new SqlConnection("connectionhere"))
            {
                return con.QueryFirstOrDefault<T>(
                   @"sqlhere",
                   commandType: CommandType.Text,
                   param: new
                   {
                       Token = new DbString
                       {
                           Value = paramvalue,
                           Length = 100,
                           IsAnsi = true
                       }
                   }
               );
            }
            
            ```
