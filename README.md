This is the _unofficial_ MinIO Dart Client SDK that provides simple APIs to access any Amazon S3 compatible object storage server.

## API

| Bucket operations     	| Object operations      	| Presigned operations 	| Bucket Policy & Notification operations 	|
|-------------------------|-------------------------|-----------------------|-------------------------------------------|
| [makeBucket]           	| [getObject]            	| [presignedUrl]       	| getBucketNotification                   	|
| [listBuckets]          	| [getPartialObject]     	| presignedGetObject   	| setBucketNotification                   	|
| [bucketExists]         	| [fGetObject]           	| presignedPutObject   	| removeAllBucketNotification             	|
| [removeBucket]         	| [putObject]            	| presignedPostPolicy  	| getBucketPolicy                         	|
| [listObjects]          	| [fPutObject]           	|                      	| setBucketPolicy                         	|
| [listObjectsV2]        	| [copyObject]           	|                      	| listenBucketNotification                	|
| [listIncompleteUploads]	| [statObject]           	|                      	|                                         	|
|                       	| [removeObject]         	|                      	|                                         	|
|                       	| [removeObjects]        	|                      	|                                         	|
|                       	| [removeIncompleteUpload]|                      	|                                         	|


## Usage

### Initialize MinIO Client

**MinIO**

```dart
final minio = Minio(
  endPoint: 'play.min.io',
  accessKey: 'Q3AM3UQ867SPQQA43P2F',
  secretKey: 'zuf+tfteSlswRu7BJ86wekitnifILbZam1KYY3TG',
);
```

**AWS S3**

```dart
final minio = Minio(
  endPoint: 's3.amazonaws.com',
  accessKey: 'YOUR-ACCESSKEYID',
  secretKey: 'YOUR-SECRETACCESSKEY',
);
```

**File upload**
```dart
import 'package:minio/io.dart';
import 'package:minio/minio.dart';

void main() async {
  final minio = Minio(
    endPoint: 'play.min.io',
    accessKey: 'Q3AM3UQ867SPQQA43P2F',
    secretKey: 'zuf+tfteSlswRu7BJ86wekitnifILbZam1KYY3TG',
  );

  await minio.fPutObject('mybucket', 'myobject', 'path/to/file');
}
```

For complete example, see: [example]

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

Contributions to this repository are welcomed.

## License

MIT

[tracker]: https://github.com/xtyxtyx/minio-dart/issues
[example]: https://pub.dev/packages/minio#-example-tab-
[link text itself]: http://www.reddit.com

[makeBucket]: https://pub.dev/documentation/minio/latest/minio/Minio/makeBucket.html
[listBuckets]: https://pub.dev/documentation/minio/latest/minio/Minio/listBuckets.html
[bucketExists]: https://pub.dev/documentation/minio/latest/minio/Minio/bucketExists.html
[removeBucket]: https://pub.dev/documentation/minio/latest/minio/Minio/removeBucket.html
[listObjects]: https://pub.dev/documentation/minio/latest/minio/Minio/listObjects.html
[listObjectsV2]: https://pub.dev/documentation/minio/latest/minio/Minio/listObjectsV2.html
[listIncompleteUploads]: https://pub.dev/documentation/minio/latest/minio/Minio/listIncompleteUploads.html

[getObject]: https://pub.dev/documentation/minio/latest/minio/Minio/getObject.html
[getPartialObject]: https://pub.dev/documentation/minio/latest/minio/Minio/getPartialObject.html
[putObject]: https://pub.dev/documentation/minio/latest/minio/Minio/putObject.html
[copyObject]: https://pub.dev/documentation/minio/latest/minio/Minio/copyObject.html
[statObject]: https://pub.dev/documentation/minio/latest/minio/Minio/statObject.html
[removeObject]: https://pub.dev/documentation/minio/latest/minio/Minio/removeObject.html
[removeObjects]: https://pub.dev/documentation/minio/latest/minio/Minio/removeObjects.html
[removeIncompleteUpload]: https://pub.dev/documentation/minio/latest/minio/Minio/removeIncompleteUpload.html

[fGetObject]: https://pub.dev/documentation/minio/latest/io/MinioX/fGetObject.html
[fPutObject]: https://pub.dev/documentation/minio/latest/io/MinioX/fPutObject.html

[presignedUrl]: https://pub.dev/documentation/minio/latest/minio/Minio/presignedUrl.html

