cropper插件相关配置项:

(1)
    <script src="/assets/lib/jquery.js"></script>
    <script src="/assets/lib/cropper/Cropper.js"></script>
    <script src="/assets/lib/cropper/jquery-cropper.js"></script>

(2)
    <link rel="stylesheet" href="/assets/lib/cropper/cropper.css">

(3)
    <div class="row1">
                <!-- 图片裁剪区域 -->
                <div class="cropper-box">
                    <!-- 这个 img 标签很重要，将来会把它初始化为裁剪区域 -->
                    <img id="image" src="/assets/images/sample.jpg" />
                </div>
                <!-- 图片的预览区域 -->
                <div class="preview-box">
                    <div>
                        <!-- 宽高为 100px 的预览区域 -->
                        <div class="img-preview w100"></div>
                        <p class="size">100 x 100</p>
                    </div>
                    <div>
                        <!-- 宽高为 50px 的预览区域 -->
                        <div class="img-preview w50"></div>
                        <p class="size">50 x 50</p>
                    </div>
                </div>
            </div>

            <!-- 第二行的按钮区域 -->
            <div class="row2">
                <!-- 通过accept属性，可以指定，允许用户选择什么类型的文件 -->
                <input type="file" id="file" accept="image/png,image/jpeg">
                <button type="button" class="layui-btn" id="btnChooseImage">上传</button>
                <button type="button" class="layui-btn layui-btn-danger" id="btnUpload">确定</button>
            </div>

(4)
    $(function () {
        // 1.1 获取裁剪区域的 DOM 元素(将某个图片初始化为裁剪区域)
        var $image = $('#image')
        // 1.2 配置选项
        const options = {
            // 纵横比
            aspectRatio: 1,
            // 指定预览区域
            preview: '.img-preview'
        }
    
        // 1.3 创建裁剪区域
        $image.cropper(options)
    
    })