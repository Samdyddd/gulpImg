# gulpImg
通过node+gulp做一个前端图片压缩工具
## 通过node调用gulp配置文件中可以调用各种工具压缩图片：gulp-imagemin和雅虎的imagemin-pngquant.
配置如下：
var gulp = require('gulp'),
    imagemin = require('gulp-imagemin');
    //多任务
    gulp.task('default',function(){gulp.run('minify-img');});
gulp.task('minify-img',function(){
    gulp.src('index/image/*')
      .pipe(imagemin())
      .pipe(gulp.dest('dest/image')):
})

//通过node的fs包导入文件。
