# Phone Number Validation API
_Developed by Rohan Paudel_

> [!NOTE]
> This project has been developed and designed to provide a freemium phone number validation service across the globe.

## Overview
The Phone Number Details API provides information about phone numbers, including region, type, validity, and more.

## Endpoint

**Get Phone Number Details**

- **URL:** `https://phonenumberutils.gorkhacloud.com/phonenumberdetails`
- **Method:** GET

### Query Parameter

- **phoneNumber:** The phone number you want to check.
- > [!WARNING]
>  Ensure that the + sign in the country code is URL-encoded as `%2b`.

**Example Request:**

https://phonenumberutils.gorkhacloud.com/phonenumberdetails?phoneNumber=%2b9779864987764

## Response

## Title
**Phone Number Result**

## Message
**Please refer to data object for complete information**

## Data Object

- **region**: The name of the region associated with the phone number.
  - Example: "Nepal"
  
- **regionCode**: The ISO 3166-1 alpha-2 code for the region.
  - Example: "NP"

- **numberType**: The type of phone number. Possible values are:
  - **MOBILE**: Indicates a mobile phone number.
  - **FIXED_LINE**: Indicates a fixed-line (landline) phone number.
  - **FIXED_LINE_OR_MOBILE**: Indicates that the phone number could be either a fixed-line or a mobile phone number.
  - **UNKNOWN**: Indicates that the type of the phone number is unknown.
  - Example: "MOBILE"

- **isValid**: A boolean indicating whether the phone number is valid.
  - Example: `true`

- **countryCode**: The country calling code for the region.
  - Example: 977

- **flag**: The emoji flag representing the region.
  - Example: "🇳🇵"

- **nationalMobileNumber**: The national format of the mobile phone number.
  - Example: "9864987764"

- **informationalMessage**: A message providing additional information about the phone number.
  - Example: "Phone number is valid."

## Example JSON Response

```json
{
    "title": "Phone Number Result",
    "message": "Please refer to data object for complete information",
    "data": {
        "region": "Nepal",
        "regionCode": "NP",
        "numberType": "MOBILE",
        "isValid": true,
        "countryCode": 977,
        "flag": "🇳🇵",
        "nationalMobileNumber": "9864987764",
        "informationalMessage": "Phone number is valid."
    }
}
