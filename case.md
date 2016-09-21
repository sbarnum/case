
- [Enumeration](#enumeration)
- [Supporting Classes](#supporting-classes)
- [Object](#object)
- [Property Bundle](#property-bundle)

# Enumeration





### ByteOrder


**SubTypes:**  BigEndian, LittleEndian



### CompressionMethod


**SubTypes:**  BZIP2, Deflate, LZMA, XZ, ZLIB



### DataType




### EncodingMethod


**SubTypes:**  Base16, Base32, Base64



### EncryptionMethod


**SubTypes:**  AES, Blowfish, DES, DES3, RC4



### EncryptionMode


**SubTypes:**  CBC, CFB, ECB, OFB



### ErrorType


**SubTypes:**  Critical, Debug, Error, Info, Warning



### FileMismatchType




### FileSystemType


**SubTypes:**  BDEVolume, CPIO, Compressed, DataRange, EWF, EXT4, Encoded, Encrypted, F2FS, NTFS, SQLiteBlob, SevenZ, TAR, VSSVolume, Volume, ZIP



### HashMethod


**SubTypes:**  MD5, SHA, SHA-1, SHA-2



### ImageCompressionMethod


**SubTypes:**  BMP, Huffman, JPEG, LZW, PNG, TIFF, WebP



### Language
TODO: We probably can use an already existing schema for this.

**SubTypes:**  English, French, Spanish



### MimeType




### PEType




### ServiceStatus




### Servicetype




### StartType




### VisibilityType


**SubTypes:**  Private, Public



# Supporting Classes





### DictionaryItem


Attribute | Range | Comment
---: | --- | ---
*key* | xsd:string | 
*value* | xsd:string | 


### DomainName


Attribute | Range | Comment
---: | --- | ---
*isTLD* | xsd:boolean | 
*value* | xsd:string | 


### EmailAddress
TODO: Merge this into EmailAccount?

Attribute | Range | Comment
---: | --- | ---
*stringValue* | xsd:string | 


### FilePath
TODO: Determine if this object is wanted, or if we want to stick with strings.

Attribute | Range | Comment
---: | --- | ---
*delimiter* | xsd:string | 
*filePathSegments* | olo:OrderedList | 


### IPv4Address


Attribute | Range | Comment
---: | --- | ---
*value* | xsd:string | 


### IPv6Address


Attribute | Range | Comment
---: | --- | ---
*value* | xsd:string | 


### MACAddress


Attribute | Range | Comment
---: | --- | ---
*value* | xsd:string | 


### URI


Attribute | Range | Comment
---: | --- | ---
*value* | xsd:string | 


### WindowsPEFileHeader
Properties of the PE file header, sometimes referred to as the COFF header.

Attribute | Range | Comment
---: | --- | ---
*characteristics* | xsd:hexBinary | 
*hash* | [Hash](#hash) | TODO: Remove this use of this property in exchange for using the Hash property bundle.
*machine* | xsd:hexBinary | 
*numberOfSections* | xsd:hexBinary | 
*numberOfSymbols* | xsd:hexBinary | 
*optionalHeader* | [WindowsPEOptionalHeader](#windowspeoptionalheader) | 
*pointerToSymbolTable* | xsd:hexBinary | 
*sizeOfOptionalHeader* | xsd:hexBinary | 
*timeDateStamp* | xsd:hexBinary | 


### WindowsPEOptionalHeader


Attribute | Range | Comment
---: | --- | ---
*addressOfEntryPoint* | xsd:hexBinary | 
*baseOfCode* | xsd:hexBinary | 
*checksum* | xsd:hexBinary | 
*dllCharacteristics* | xsd:hexBinary | 
*entropy* | xsd:float | 
*fileAlignment* | xsd:hexBinary | 
*hash* | [Hash](#hash) | TODO: Remove this use of this property in exchange for using the Hash property bundle.
*imageBase* | xsd:hexBinary | 
*loaderFlags* | xsd:hexBinary | 
*magic* | xsd:hexBinary | 
*majorImageVersion* | xsd:hexBinary | 
*majorOSVersion* | xsd:hexBinary | 
*majorSubsystemVersion* | xsd:hexBinary | 
*majorlinkerVersion* | xsd:hexBinary | 
*minorImageVersion* | xsd:hexBinary | 
*minorLinkerVersion* | xsd:hexBinary | 
*minorOSVersion* | xsd:hexBinary | 
*minorSubsystemVersion* | xsd:hexBinary | 
*numberOfRVAAndSizes* | xsd:hexBinary | 
*sectionAlignment* | xsd:hexBinary | 
*sizeOfCode* | xsd:hexBinary | 
*sizeOfHeaders* | xsd:hexBinary | 
*sizeOfHeapCommit* | xsd:hexBinary | 
*sizeOfHeapReserve* | xsd:hexBinary | 
*sizeOfImage* | xsd:hexBinary | 
*sizeOfInitializedData* | xsd:hexBinary | 
*sizeOfStackCommit* | xsd:hexBinary | 
*sizeOfStackReserve* | xsd:hexBinary | 
*sizeOfUnintialializedData* | xsd:hexBinary | 
*subsystem* | xsd:hexBinary | 
*win32VersionValue* | xsd:hexBinary | 


### WindowsPESection


Attribute | Range | Comment
---: | --- | ---
*hash* | [Hash](#hash) | TODO: Remove this use of this property in exchange for using the Hash property bundle.
*name* | xsd:string | The name property defines a common word or phrase that describes the meaning of the object.
*size* | xsd:positiveInteger | Size of file in bytes.


### WindowsRegistryValue


Attribute | Range | Comment
---: | --- | ---
*dataType* | [DataType](#datatype) | 
*name* | xsd:string | The name property defines a common word or phrase that describes the meaning of the object.
*value* | xsd:string | 


### X509V3Extensions


Attribute | Range | Comment
---: | --- | ---
*authorityKeyIdentifier* | xsd:string | 
*basicContraints* | xsd:string | 
*certificatePolicies* | xsd:string | 
*crlDistributionPoints* | xsd:string | 
*extendedKeyUsage* | xsd:string | 
*inhibitAnyPolicy* | xsd:string | 
*issuerAlternativeName* | xsd:string | 
*keyUsage* | xsd:string | 
*nameContraints* | xsd:string | 
*policyConstraints* | xsd:string | 
*policyMappings* | xsd:string | 
*privateKeyUsagePeriodNotAfter* | xsd:dateTimeStamp | 
*privateKeyUsagePeriodNotBefore* | xsd:dateTimeStamp | 
*subjectAlternativeName* | xsd:string | 
*subjectDirectoryAttribute* | xsd:string | 
*subjectKeyIdentifier* | xsd:string | 


# Object



Attribute | Range | Comment
---: | --- | ---
*location* | [Location](#location) | 
*propertyBundle* | [PropertyBundle](#propertybundle) | 


### Descriptive

A Descriptive object allows the use of the name and description property.

Attribute | Range | Comment
---: | --- | ---
*description* | xsd:string | 
*name* | xsd:string | The name property defines a common word or phrase that describes the meaning of the object.


##### Action


Attribute | Range | Comment
---: | --- | ---
*actionLifecyclePhase* | [ActionLifecyclePattern](#actionlifecyclepattern) | 
*endTime* | xsd:dateTimeStamp | 
*environment* | [Object](#object) | Defines the environment of an Action. This can point to things like the descriptions of the area the action was performed or information about the computer that was used.
*instrument* | [Object](#object) | The instrument the acutator used to perform the action. (This is usually an item that contains a tool property bundle.)
*performer* | [Object](#object) | Defines the person, action, or thing that caused this action.
*result* | [Object](#object) | 
*source* | [Object](#object) | 
*startTime* | xsd:dateTimeStamp | 


##### ActionLifecyclePattern
Defines an ordered list that must contain only Action classes as items.



##### Annotation


Attribute | Range | Comment
---: | --- | ---
*object* | [Object](#object) | 
*tag* | xsd:string | 


##### Identity


Attribute | Range | Comment
---: | --- | ---
*associatedAccount* | (Restriction on property [propertyBundle](#propertybundle) with [owl:minQualifiedCardinality (1 : xsd:nonNegativeInteger), owl:onClass [PropertyBundle](#propertybundle)]), [Object](#object) | References objects with an account property bundle.
*organization* | xsd:string | 


##### Investigation


Attribute | Range | Comment
---: | --- | ---
*endAction* | [Action](#action) | 
*forensicActions* | (Restriction on property olo:slot with [owl:allValuesFrom (Restriction on property olo:item with [owl:allValuesFrom [ForensicAction](#forensicaction)])]), olo:OrderedList | 
*investigator* | ([Identity](#identity) or [Role](#role)) | 
*startAction* | [Action](#action) | 
*subject* | ([Identity](#identity) or [Role](#role)), xsd:string | 
*suspectedOffense* | xsd:string | 
*victim* | ([Identity](#identity) or [Role](#role)) | 


##### Location




##### ProvenanceRecord


Attribute | Range | Comment
---: | --- | ---
*exhibitNumber* | xsd:string | 
*object* | [Object](#object) | 


##### Relationship


Attribute | Range | Comment
---: | --- | ---
*bidirectional* | xsd:boolean | 
*destination* | [Object](#object) | 
*endTime* | xsd:dateTimeStamp | 
*kindOfRelationship* | xsd:string | 
*source* | [Object](#object) | 
*startTime* | xsd:dateTimeStamp | 


##### Role


Attribute | Range | Comment
---: | --- | ---
*object* | [Object](#object) | 


##### Tool
TODO: How does "Tool", "Software", and "Application" relate to each other?

Attribute | Range | Comment
---: | --- | ---
*vendor* | xsd:string | 
*version* | xsd:string | 


##### Trace
An object that must contain at least one property bundle.



# Property Bundle





### AFFImage




### Account


Attribute | Range | Comment
---: | --- | ---
*accountIssuer* | xsd:string | 
*createdTime* | xsd:dateTimeStamp | 
*displayName* | xsd:string | 
*expiredTime* | xsd:dateTimeStamp | 
*identifier* | xsd:string | 
*isActive* | xsd:boolean | 


### AccountAuthentication


Attribute | Range | Comment
---: | --- | ---
*password* | xsd:string | 
*passwordLastChanged* | xsd:dateTimeStamp | 


### AndroidPackage




### Application


Attribute | Range | Comment
---: | --- | ---
*identifier* | xsd:string | 
*numberOfLaunches* | xsd:positiveInteger | 
*operatingSystem* | (Restriction on property [propertyBundle](#propertybundle) with [owl:someValuesFrom [OperatingSystem](#operatingsystem)]), [Trace](#trace) | 
*version* | xsd:string | 


### ApplicationAccount


Attribute | Range | Comment
---: | --- | ---
*application* | [Trace](#trace) | Defines the application-like item used by this account.


### ArchiveFile
Defines the basic properties associated with an archive file system.

Attribute | Range | Comment
---: | --- | ---
*comment* | xsd:string | 
*version* | xsd:string | 


### Attachment
Defines an object that is an attachment of a message.

Note: This property bundle is different. Instead of putting this as a property bundle of the attachment itself, you put this on the message.

Attribute | Range | Comment
---: | --- | ---
*mimeType* | [MimeType](#mimetype) | 
*object* | [Object](#object) | 


### Audio




### BDEVolume
The Bitlocker Drive Encryption (BDE) credentials.

Attribute | Range | Comment
---: | --- | ---
*password* | xsd:string | 
*recoveryPassword* | xsd:string | 
*startupKey* | xsd:base64Binary | 


### BrowserBookmark




### BrowserCookie




### BrowserHistory




### ByteRun




### Compressed
Defines the basic properties associated with a compressed stream.

Attribute | Range | Comment
---: | --- | ---
*compressionMethod* | [CompressionMethod](#compressionmethod) | 


### ComputerSpecifications


Attribute | Range | Comment
---: | --- | ---
*bios* | xsd:string | 
*cpu* | xsd:string | 
*ram* | xsd:string | 


### Contact




### ContentData


Attribute | Range | Comment
---: | --- | ---
*byteOrder* | [ByteOrder](#byteorder) | 
*data* | xsd:base64Binary | 
*size* | xsd:positiveInteger | Size of file in bytes.


### DataRange
Defines the basic properties associated with a range of data.

Attribute | Range | Comment
---: | --- | ---
*rangeOffset* | xsd:positiveInteger | 
*rangeSize* | xsd:positiveInteger | 


### Device


Attribute | Range | Comment
---: | --- | ---
*manufacturer* | xsd:string | 
*model* | xsd:string | 
*serialNumber* | xsd:string | 


### DigitalAccount


Attribute | Range | Comment
---: | --- | ---
*accountLogin* | xsd:string | 
*firstLoginTime* | xsd:dateTimeStamp | 
*lastLoginTime* | xsd:dateTimeStamp | 


### Disk




### DiskPartition


Attribute | Range | Comment
---: | --- | ---
*partIndex* | xsd:positiveInteger | 


### EWFImage


Attribute | Range | Comment
---: | --- | ---
*acquiryDate* | xsd:dateTimeStamp | 
*caseNumber* | xsd:integer | 
*compressionMethod* | [CompressionMethod](#compressionmethod) | 
*description* | xsd:string | 
*errorGranularity* | xsd:integer | 
*evidenceNumber* | xsd:string | 
*examinerName* | xsd:string | 
*format* | xsd:string | 
*guid* | xsd:string | 
*notes* | xsd:string | 
*operatingSystemUsed* | xsd:string | 
*password* | xsd:string | 
*sectorsPerChunk* | xsd:integer | 
*softwareVersionUsed* | xsd:string | 
*systemDate* | xsd:dateTimeStamp | 


### EXIF
TODO: Use imported exif ontology

Attribute | Range | Comment
---: | --- | ---
*exifData* | [DictionaryItem](#dictionaryitem) | 


### EmailAccount


Attribute | Range | Comment
---: | --- | ---
*emailAddress* | xsd:string | 


### EmailMessage




### Encoded


Attribute | Range | Comment
---: | --- | ---
*encodingMethod* | [EncodingMethod](#encodingmethod) | 


### Encrypted


Attribute | Range | Comment
---: | --- | ---
*encryptionIV* | xsd:hexBinary | 
*encryptionKey* | xsd:hexBinary | 
*encryptionMethod* | [EncryptionMethod](#encryptionmethod) | 
*encryptionMode* | [EncryptionMode](#encryptionmode) | 


### Error




### Event




### ExtractedFeatures


Attribute | Range | Comment
---: | --- | ---
*extractedCodeSnippet* | (Restriction on property [propertyBundle](#propertybundle) with [owl:someValuesFrom [ExtractedString](#extractedstring)]), [Trace](#trace) | 
*extractedImport* | (Restriction on property [propertyBundle](#propertybundle) with [owl:someValuesFrom [ExtractedString](#extractedstring)]), [Trace](#trace) | 
*extractedString* | (Restriction on property [propertyBundle](#propertybundle) with [owl:someValuesFrom [ExtractedString](#extractedstring)]), [Trace](#trace) | 


### ExtractedString


Attribute | Range | Comment
---: | --- | ---
*byteStringValue* | xsd:base64Binary | 
*encodingMethod* | [EncodingMethod](#encodingmethod) | 
*englishTranslation* | xsd:string | 
*hash* | [Hash](#hash) | TODO: Remove this use of this property in exchange for using the Hash property bundle.
*language* | [Language](#language) | 
*length* | xsd:integer | 
*stringValue* | xsd:string | 


### File
Represents a file.

TODO: Not sure what properties should be in here versus being in Data or FileSystem.

Attribute | Range | Comment
---: | --- | ---
*magicNumber* | xsd:base64Binary | 
*mimeType* | [MimeType](#mimetype) | 


### FileMetadataMismatch


Attribute | Range | Comment
---: | --- | ---
*mismatchType* | [FileMismatchType](#filemismatchtype) | 


### FileSystem
Defines the basic properties associated with the storage of a file on a file system.

Attribute | Range | Comment
---: | --- | ---
*accessedTime* | xsd:dateTimeStamp | 
*createdTime* | xsd:dateTimeStamp | 
*extension* | xsd:string | The file extension.
*fileName* | xsd:string | 
*filePath* | [FilePath](#filepath) | 
*fileSystemType* | [FileSystemType](#filesystemtype) | 
*inode* | xsd:integer | 
*isDirectory* | xsd:boolean | 
*modifedTime* | xsd:dateTimeStamp | 
*parentFileSystem* | (Restriction on property [propertyBundle](#propertybundle) with [owl:onClass [FileSystem](#filesystem), owl:qualifiedCardinality (1 : xsd:nonNegativeInteger)]), [Trace](#trace) | The parent property must point to an Item type that has at exactly one dfvfs property within it.
*size* | xsd:positiveInteger | Size of file in bytes.


### HTTPConnection


Attribute | Range | Comment
---: | --- | ---
*httpMessageBodyData* | xsd:base64Binary | 
*httpMessageBodyLength* | xsd:integer | 
*httpRequestHeader* | xsd:base64Binary | 
*httpRequestLine* | xsd:base64Binary | 


### Hash


Attribute | Range | Comment
---: | --- | ---
*hashMethod* | [HashMethod](#hashmethod) | 
*hashValue* | xsd:hexBinary | 


### ICMPConnection


Attribute | Range | Comment
---: | --- | ---
*code* | xsd:string | 


### IOSPackage




### Image
Defines the basic properties associated with a disk image file. (Ie. the full image of a disk, not just specific volumes.)



### LVMVolume




### LinuxPackage




### Memory




### Message


Attribute | Range | Comment
---: | --- | ---
*body* | xsd:string | 
*participant* |  | A participant of the Message.
*sender* |  | The sender of the message.


### MessageThread


Attribute | Range | Comment
---: | --- | ---
*displayName* | xsd:string | 
*identifier* | xsd:string | 
*messages* | (Restriction on property olo:slot with [owl:allValuesFrom (Restriction on property olo:item with [owl:allValuesFrom (Restriction on property [propertyBundle](#propertybundle) with [owl:someValuesFrom [Message](#message)])])]), olo:OrderedList | 
*visibility* | [VisibilityType](#visibilitytype) | 


### Mutex


Attribute | Range | Comment
---: | --- | ---
*name* | xsd:string | The name property defines a common word or phrase that describes the meaning of the object.


### NTFS


Attribute | Range | Comment
---: | --- | ---
*alternateDataStream* | xsd:string | 
*sid* | xsd:string | 


### NetworkConnection


Attribute | Range | Comment
---: | --- | ---
*destination* | [Object](#object) | 
*endTime* | xsd:dateTimeStamp | 
*protocols* |  | 
*source* | [Object](#object) | 
*startTime* | xsd:dateTimeStamp | 


### NetworkLocation


Attribute | Range | Comment
---: | --- | ---
*domain* | xsd:string | 
*ipAddress* | xsd:string | Change this to an already defined ip address type.


### NetworkPacket




### NetworkRoute




### NetworkSocket




### NetworkSubnet




### OperatingSystem


Attribute | Range | Comment
---: | --- | ---
*manufacturer* | xsd:string | 
*version* | xsd:string | 


### PDFFile


Attribute | Range | Comment
---: | --- | ---
*documentInformation* |  | 
*isOptimized* | xsd:boolean | 
*pdfId0* | xsd:string | 
*pdfId1* | xsd:string | 
*version* | xsd:string | 


### Package
Defines a software application package.

TODO: Determine which of these properties are valid and which need to go into a specific property bundle (AndoridPackage, iOSPackage, LinuxPackage, etc.)

Attribute | Range | Comment
---: | --- | ---
*applicationName* | xsd:string | The name of the application (friendly name)
*dataPath* | [Trace](#trace) | Path designated by the OS to be used by that package application.
*packageName* | xsd:string | The package name (identifier)
*packagePermission* | xsd:string | Defines a permission associated with the application.
*version* | xsd:string | 


### PhoneAccount


Attribute | Range | Comment
---: | --- | ---
*phoneNumber* | xsd:string | 


### PhoneCall


Attribute | Range | Comment
---: | --- | ---
*participant* |  | A participant of the Message.
*sender* |  | The sender of the message.


### Process


Attribute | Range | Comment
---: | --- | ---
*arguments* | xsd:string | 
*binary* | [Trace](#trace) | 
*createdTime* | xsd:dateTimeStamp | 
*creatorUser* | [Trace](#trace) | 
*currentWorkingDirectory* | [FilePath](#filepath) | 
*environmentVariable* | [DictionaryItem](#dictionaryitem) | 
*isHidden* | xsd:boolean | 
*parentProcess* | (Restriction on property [propertyBundle](#propertybundle) with [owl:minQualifiedCardinality (1 : xsd:nonNegativeInteger), owl:onClass [Process](#process)]), [Trace](#trace) | 
*pid* | xsd:integer | 


### QCOWImage




### RasterPicture


Attribute | Range | Comment
---: | --- | ---
*bitsPerPixel* | xsd:integer | 
*format* | xsd:string | 
*imageCompressionMethod* | [ImageCompressionMethod](#imagecompressionmethod) | 
*imageHeight* | xsd:positiveInteger | 
*imageWidth* | xsd:positiveInteger | 


### SMSMessage




### SQLiteBlob


Attribute | Range | Comment
---: | --- | ---
*columnName* | xsd:string | 
*rowCondition* | xsd:string | 
*rowIndex* | xsd:positiveInteger | 
*tableName* | xsd:string | 


### SymbolicLink




### System




### TCPConnection


Attribute | Range | Comment
---: | --- | ---
*destinationFlags* | xsd:string | 
*destinationPort* | xsd:integer | 
*sourceFlags* | xsd:string | 
*sourcePort* | xsd:integer | 


### ToolArguments




### UDPConnection


Attribute | Range | Comment
---: | --- | ---
*destinationPort* | xsd:integer | 
*sourcePort* | xsd:integer | 


### UNIXAccount
Properties specific to an account on a UNIX system

Attribute | Range | Comment
---: | --- | ---
*gid* | xsd:integer | 
*group* | xsd:string | 
*shell* | xsd:string | 


### UNIXNetworkRoute




### UNIXProcess




### UNIXVolume




### UserAccount
Properties of an instance of a user account on a system.

Attribute | Range | Comment
---: | --- | ---
*canEscalatePrivs* | xsd:boolean | 
*homeDirectory* | [FilePath](#filepath) | 
*isPrivileged* | xsd:boolean | 
*isServiceAccount* | xsd:boolean | 


### VHDIImage




### VMDKImage




### VSSVolume


Attribute | Range | Comment
---: | --- | ---
*snapshotID* | xsd:string | 


### Volume




### WHOIS




### WindowsAccount
Properties specific to an account on a Microsoft Windows (tm) system.

Attribute | Range | Comment
---: | --- | ---
*group* | xsd:string | 


### WindowsMutex




### WindowsNetworkRoute




### WindowsPEBinaryFile


Attribute | Range | Comment
---: | --- | ---
*fileHeader* | [WindowsPEFileHeader](#windowspefileheader) | 
*impHash* | xsd:string | 
*peType* | [PEType](#petype) | 
*sections* | [WindowsPESection](#windowspesection) | 


### WindowsPackage




### WindowsPrefetchFile




### WindowsProcess


Attribute | Range | Comment
---: | --- | ---
*aslrEnabled* | xsd:boolean | 
*depEnabled* | xsd:boolean | 
*ownerSID* | xsd:string | 
*priority* | xsd:string | 
*startupInfo* |  | 
*windowsTitle* | xsd:string | 


### WindowsRegistryKey


Attribute | Range | Comment
---: | --- | ---
*creator* | [Trace](#trace) | 
*key* | xsd:string | 
*modifedTime* | xsd:dateTimeStamp | 
*numberOfSubkeys* | xsd:integer | 
*registryValue* | [WindowsRegistryValue](#windowsregistryvalue) | 


### WindowsService


Attribute | Range | Comment
---: | --- | ---
*displayName* | xsd:string | 
*group* | xsd:string | 
*serviceStatus* | [ServiceStatus](#servicestatus) | 
*serviceType* | [Servicetype](#servicetype) | 
*startCommandLine* | xsd:string | 
*startType* | [StartType](#starttype) | 


### WindowsSystem




### WindowsVolume




### X509Certificate


Attribute | Range | Comment
---: | --- | ---
*hash* | [Hash](#hash) | TODO: Remove this use of this property in exchange for using the Hash property bundle.
*isSelfSigned* | xsd:boolean | 
*issuer* | xsd:string | 
*serialNumber* | xsd:string | 
*signatureAlgorithm* | xsd:string | 
*subject* | ([Identity](#identity) or [Role](#role)), xsd:string | 
*subjectPublicKeyAlgorithm* | xsd:string | 
*subjectPublicKeyExponent* | xsd:integer | 
*subjectPublicKeyModulus* | xsd:string | 
*validityNotAfter* | xsd:dateTimeStamp | 
*validityNotBefore* | xsd:dateTimeStamp | 
*version* | xsd:string | 
*x509V3Extensions* | [X509V3Extensions](#x509v3extensions) | 

