# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [greenvector.proto](#greenvector-proto)
    - [FacetVector](#green_vector-FacetVector)
    - [GreenVectorReply](#green_vector-GreenVectorReply)
    - [GreenVectorRequest](#green_vector-GreenVectorRequest)
    - [InputVector](#green_vector-InputVector)
    - [InputVector.FacetWeightsEntry](#green_vector-InputVector-FacetWeightsEntry)
  
    - [GreenVectors](#green_vector-GreenVectors)
  
- [Scalar Value Types](#scalar-value-types)



<a name="greenvector-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## greenvector.proto



<a name="green_vector-FacetVector"></a>

### FacetVector



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| facet | [string](#string) |  |  |
| vector | [float](#float) | repeated |  |
| count | [uint64](#uint64) |  |  |
| average_weight | [float](#float) |  |  |






<a name="green_vector-GreenVectorReply"></a>

### GreenVectorReply



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| facet_vectors | [FacetVector](#green_vector-FacetVector) | repeated |  |






<a name="green_vector-GreenVectorRequest"></a>

### GreenVectorRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| facet_vectors | [FacetVector](#green_vector-FacetVector) | repeated |  |
| input_vectors | [InputVector](#green_vector-InputVector) | repeated |  |






<a name="green_vector-InputVector"></a>

### InputVector



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| vector | [float](#float) | repeated |  |
| facet_weights | [InputVector.FacetWeightsEntry](#green_vector-InputVector-FacetWeightsEntry) | repeated |  |






<a name="green_vector-InputVector-FacetWeightsEntry"></a>

### InputVector.FacetWeightsEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [float](#float) |  |  |





 

 

 


<a name="green_vector-GreenVectors"></a>

### GreenVectors


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| CreateBatch | [GreenVectorRequest](#green_vector-GreenVectorRequest) | [GreenVectorReply](#green_vector-GreenVectorReply) |  |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

