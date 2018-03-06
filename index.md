## Welcome to GitHub Pages
<script>
  var userAgent = navigator.userAgent.toLowerCase();
  if (navigator.userAgent.match(/iPhone/i) || userAgent == "xsq_id_ios") {
    var mobiscroll_theme = 'ios',
        mobiscroll_display = 'bottom';
  } else {
    var mobiscroll_theme = 'android-holo-light',
        mobiscroll_display = 'center';
  }
  var currYear = (new Date()).getFullYear();    
  var opt={};
  opt.date = {preset : 'date'};
  opt.datetime = {preset : 'datetime'};
  opt.time = {preset : 'time'};
  opt.default = {
    theme: mobiscroll_theme,
    display: mobiscroll_display,
    mode: 'scroller',
    lang:'zh'
  };
  opt.default_validator = {
    theme: mobiscroll_theme,
    display: mobiscroll_display,
    mode: 'scroller',
    lang:'zh',
    onSet:function(valueText,inst){
      $('#demo2').data('bootstrapValidator')  
      .updateStatus('name', 'NOT_VALIDATED',null)  
      .validateField('name'); 
    }
  };
  var optDateValidator = $.extend(opt['date'], opt['default_validator']);
  var optDate = $.extend(opt['date'], opt['default']);
  var optDateTime = $.extend(opt['datetime'], opt['default']);
  var optTime = $.extend(opt['time'], opt['default']);
  $("#demo1").mobiscroll(optDateValidator);
  $("#demo2").mobiscroll(optDateTime);
  $("#demo3").mobiscroll(optDate);
  $("#demo4").mobiscroll(optDate);
  $("#demo5").mobiscroll(optDate);