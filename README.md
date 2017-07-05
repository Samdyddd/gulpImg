# gulpImg
通过node+gulp做一个前端图片压缩工具
## 通过node调用gulp配置文件中可以调用各种工具压缩图片：gulp-imagemin和雅虎的imagemin-pngquant.
配置如下：
var gulp = require('gulp'),<br>
    imagemin = require('gulp-imagemin');<br>
    //多任务<br>
    gulp.task('default',function(){gulp.run('minify-img');});<br>
gulp.task('minify-img',function(){<br>
    gulp.src('index/image/*')<br>
      .pipe(imagemin())<br>
      .pipe(gulp.dest('dest/image')):<br>
})<br>
<br>
## 通过node的fs包导入文件。
