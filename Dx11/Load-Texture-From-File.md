

首先參考官方的說法: [How to: Initialize a Texture From a File](
http://msdn.microsoft.com/en-us/library/windows/desktop/ff476904%28v=vs.85%29.aspx)

但是這個方法很繁瑣，所以可以考慮使用一些比較方便的庫，如 DirectXTex 或 DirectXTK

DirectXTex 有兩個方法 LoadDDSFromFile() 和 CreateTexture()，互相搭配就可以建立 Texture2D

```cpp

DirectX::TexMetadata kMetaData;
DirectX::ScratchImage kImage;
HRESULT hr = LoadFromDDSFile( strTexFilePath.c_str(), DDS_FLAGS_NONE, &kMetaData, kImage ) );

DirectX::CreateTextureEx( GetDevice(), 
                          kImage.GetImages(), kImage.GetImageCount(), kImage.GetMetadata(),
                          D3D11_USAGE_DEFAULT, 
                          D3D11_BIND_SHADER_RESOURCE, 
                          0, 0, false, 
                          reinterpret_cast< ID3D11Resource** >( &pTexture2D ) ) );
```

參考連結
- [DirectXTex](http://directxtex.codeplex.com/)
