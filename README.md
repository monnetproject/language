Monnet Language Interface
=========================

Monnet Language Interface replacing Java's built-in `Locale` class with a richer model
compliant with ISO-639, ISO-3166-1, ISO-15924 and RFC 4646.

Features
--------


 * all languages specified in ISO 639-1 are represented here, and others can be
 * created as desired. Languages can be obtained as follows:
     - Directly, e.g., `Language.ENGLISH`
     - By defining a regional or script variation, e.g., `Language.ENGLISH.getRegionalVariant(Region.UNITED_KINGDOM)`
     - By looking up an ISO code `Language.getByIso639_1("en")`
     - By looking up an IETF code `Language.get("en-GB")`
     - By creating a new instance `Language.getInstance("German","Deutsch","de","deu","deu")`

 * Language tags follow the IETF language tag model, as described in RFC 4646. The format of the tags is as follows: 
    language (-script)? (-region)? (-variant)* (-extension)* (-privateuse)?
 * The string form of these may be obtained as follows 
      - The full tag can be obtained by calling `toString()`
      - The language by calling `getIso639_1()` (two letter code), `getIso639_2()` or `getIso639_3()` (three letter code)
      - The script by calling `getScript()`
      - The region by calling `getRegion()`
      - The variant(s) by calling `getVariants()`
      - The extension(s) by calling `getExtensions()`
      - The private use by calling `getPrivateUse()`

