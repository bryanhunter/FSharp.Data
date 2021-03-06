#### 1.0.0 - December 13 2012
* Initial release

#### 1.0.1 - December 14 2012
* Latest version to match with the documentation.

#### 1.0.2 - December 14 2012
* Improved method naming.

#### 1.0.4 - December 17 2012
* Improved method naming.

#### 1.0.5 - December 20 2012
* CSV provider now supports dates.

#### 1.0.6 - December 23 2012
* Build the library using .NET 4.0.

#### 1.0.8 - January 04 2013
* Support global unification in XML type provider.

#### 1.0.9 - January 04 2013
* Minor changes to support Experimental release.

#### 1.0.10 - January 06 2013
* CSV provider supports alternative separators and N/A values.

#### 1.0.11 - January 14 2013
* Support for different culture settings and CSV parsing according to RFC standard.

#### 1.0.12 - January 14 2013
* Minor update in missing fields handling.

#### 1.0.13 - January 16 2013
* Fix boolean parsing bug and improve CSV provider.

#### 1.1.0 - February 18 2013
* Support for Portable Class Libraries and Silverlight.
* Added Freebase provider.
* Improvements to the CSV provider.
* Performance improvements when handling large files.

#### 1.1.1 - February 18 2013
* Update WorldBank internals to support more efficient implementation and FunScript.

#### 1.1.2 - March 30 2013
* Update NuGet package links and icon reference.

#### 1.1.3 - April 08 2013
* Improve Units of Measure support and allow to override the type inference in the CSV Provider.

#### 1.1.4 - April 13 2013
* Allow to skip rows that don't match the schema in CsvProvider.
* Support for dynamic lookup in CSV files.
* Improvements to FSharp.Net.Http to support cookies and binary files.

#### 1.1.5 - May 13 2013
* Performance improvements, support for big csv files, and support for Guid types.
* Save, Filter and Truncate operations for csv files.

#### 1.1.6 - June 30 2013
* Fixed runtime problem accessing optional properties with a JSON null.
* Support for client certificates in FSharp.Net.Http.
* Support for Windows Phone 7.

#### 1.1.7 - July 01 2013
* Fixed problem handling enumerates in FreebaseProvider.

#### 1.1.8 - July 01 2013
* Fixed problem with portable version of FSharp.Net.Http.

#### 1.1.9 - July 21 2013
* Infer booleans for ints that only manifest 0 and 1.
* Support for partially overriding the Schema in CsvProvider.
* PreferOptionals and SafeMode parameters for CsvProvider.

#### 1.1.10 - September 12 2013
* Support for heterogeneous XML attributes.
* Make CsvFile re-entrant. 
* Support for compressed HTTP responses. 
* Fix JSON conversion of 0 and 1 to booleans.

#### 2.0.0-alpha - December 15 2013
* Support for F# 3.1 and for new portable class library projects.
* Support for sending HTTP requests with a binary body.
* Support for HTTP compression in portable class library versions (adds dependency on Zlib.Portable).
* Fixed problem when using uri's with encoded slashes (%2F) in the sample parameter of CsvProvider, JsonProvider & XmlProvider.
* CsvProvider now has GetSample static method like the other providers in addition to the default constructor.
* Add AsyncLoad(string uri) and AsyncGetSample() to CsvProvider, JsonProvider and XmlProvider.
* Removed '.AsTuple' member from CsvProvider.
* Renamed 'SampleList' static property to 'SampleIsList'.
* Renamed 'Separator' static property to 'Separators'.
* When 'SampleIsList' is true, a 'GetSamples' method is generated.
* Fixed XmlProvider's SampleIsList not working correctly.
* Fix handling of optional elements in XmlProvider when using multiple samples.
* Fix XmlProvider handling of one letter XML tags.
* Fixed CsvProvider's SafeMode not working when there were more rows than the InferRows limit.
* Exceptions raised by CsvProvider and CsvFile were reporting the wrong line number when reading files with windows line endings.
* CsvInference is now part of the runtime so it can be reused by Deedle.
* Allow currency symbols on decimals.
* Fixed file change notification not invalidating type providers correctly.
* Fix generated code doing repeated work.
* Windows Phone 7 no longer supported.
* Added Japanese documentation.
* Prevent the NuGet package from adding a reference to FSharp.Data.DesignTime.
* Entity types generated by JsonProvider & XmlProvider are now directly below the type provider, instead of under a DomainTypes inner type.
* Source Code now builds under Mono.
* Expose optional parameters from CsvFile & Http methods as optional in C#.

#### 2.0.0-alpha2 - December 24 2013
* Support heterogeneous types at the top level in XmlProvider.
* Reference System.Xml.Linq in NuGet package.
* Filter out user domains in Freebase.
* Fix Zlib.Portable being referenced by Nuget on non PCL projects.

#### 2.0.0-alpha3 - December 30 2013
* Fixed the use of samples which also are valid filenames in CsvProvider.
* Allow to specify only the Schema without a Sample in CsvProvider.

#### 2.0.0-alpha4 - January 30 2014
* Adds specific types for Freebase individuals, so each individual X only has properties P where X.P actually returns interesting data. This makes Individuals much more useful for exploring sparse data, as you can "dot" through an individual and see exactly what properties actually have interesting data. The feature is on by default but can be turned off using UseRefinedTypes=false as a static parameter.
* Individuals10 and Individuals100 views of Freebase individuals, which increases the number of items in the table by 10x and 100x.
* IndividualsAZ view of Freebase individuals, which buckets the individuals by first character of name A-Z, with each bucket containing up to 10,000 individuals.
* Added SendingQuery event which triggers for overall Freebase MQL queries and can be run in the Freebase query editor, instead of for individual REST requests including cursor-advancing requests and documentation requests.
* Renamed CsvProvider and CsvFle 'Data' property to 'Rows'.
* Renamed CsvProvider static parameter 'SafeMode' to 'AssumeMissingValues'.
* Fixed parsing of values wrapped in quotes in arrays and heterogeneous types generated by JsonProvider.
* Added SourceLink support.

#### 2.0.0-alpha5 - February 3 2014
* Renamed the 'FSharp.Data.Json.Extensions' module to 'FSharp.Data.JsonExtensions'.
* Renamed the 'FSharp.Data.Csv.Extensions' module to 'FSharp.Data.CsvExtensions'.
* Moved the contents of the 'FSharp.Net', 'FSharp.Data.Csv', and 'FSharp.Data.Json' namespaces to the 'FSharp.Data' namespace.
* Reuse identical types in JsonProvider.
* Improve JsonProvider error messages to include full path of the json part that caused the problem.
* JsonValue.ToString() now formats (indents) the output by default (can be turned off by using SaveOptions.DisableFormatting).

#### 2.0.0-alpha6 - February 4 2014
* JsonValue.Post() allows to post the JSON to the specified uri using HTTP.

#### 2.0.0-alpha7 - February 20 2014
* Improved name generation algorithm to cope better with acronymns.
* Fixed wrong singularization of words ending with 'uses'.
* Fixed handling of repeated one letter names.
* Improve HTTP error messages.
* Support for more api patterns in ApiaryProvider.
* Tolerate invalid json and missing data in apiary specifications.
* Improved naming of generated types.
* Fixed 'SampleIsList' to work with xml and json spanning multiple lines.
* Fixed handling of nested arrays in JsonProvider.
* Fixed handling of optional arrays in JsonProvider.

#### 2.0.0-beta - February 24 2014
* Mono fixes.
* Allow to set the freebase api key globally by using the environment variable FREEBASE_API_KEY
* Fixed handling of optional records in JsonProvider.
* Reduced the number of cases where heterogeneous types are used in JsonProvider.
* Fixed <type> option option being generated on some cases in JsonProvider.
* Treat "", null and missing values in the same way in JsonProvider.
* Fixed homogeneous arrays to have the same null skipping behaviour as heterogeneous arrays in JsonProvider.
* Fixed handling of optional elements in XmlProvider.
* Fixed namespace declarations generating attributes in XmlProvider.
* Fixed CsvProvider generating column names with only a space.
* Return NaN for missing data in WorldBank indicators instead of throwing an exception.
* Don't throw exceptions in JsonValue.AsArray, JsonValue.Properties, and JsonValue.InnerText.
