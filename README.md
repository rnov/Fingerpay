# Fingerpay

Fingerpay is a final last year project which aims to provide a realistic PoC of a biometric payment system relaying on cloud technology.

7 systems involved:


| machines |type               |characteristics  |
| --------:|:-----------------:|:---------------:|
| 1        | payment terminal  | with fingerprint scanner and 2 software interfaces |
| 2        | EC2 (AWS)         |    IaaS         |
| 1        | OpenShift DB      |    PaaS         |
| 3        | Dropbox           |    SaaS         |


![myimage-alt-tag](https://cloud.githubusercontent.com/assets/6912741/20408664/c112301e-ad16-11e6-8c81-38d7938c5471.png)



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    

    <title>Plotly</title>
    <link href="/favicon.ico" rel="shortcut icon" />

    



    <!-- css -->
    <link rel="stylesheet" href="//plot.ly/static/CACHE/css/8eff2b3190e9.css" type="text/css" /><link rel="stylesheet" href="//plot.ly/static/CACHE/css/cd8c3bb8280f.css" type="text/css" media="all" /><link rel="stylesheet" href="//plot.ly/static/CACHE/css/5af22aa9bb3e.css" type="text/css" />





<link rel="stylesheet" href="//plot.ly/static/CACHE/css/4836deb164f3.css" type="text/css" />
<link rel="stylesheet" type="text/css" href="//plot.ly/static/plotlycss/fonts/unified/icons.8e531060f42b.css" />



<script src="//d3nslu0hdya83q.cloudfront.net/dist/1.0/raven.min.js"></script>

<script type="text/javascript" src="//plot.ly/static/js/plugins/prettify.min.1c0e55292686.js"></script>
<script type="text/javascript" src="//plot.ly/static/js/plugins/prettify_matlab.min.89a83ec1dd7b.js"></script>
<script type="text/javascript" src="//plot.ly/static/js/plugins/prettify_r.min.db60584bbbd9.js"></script>


<!-- mixpanel -->



<!-- google analytics -->
    <script type="text/javascript">
        var _gaq = _gaq || [];
        _gaq.push(['_setAccount', 'UA-39373211-1']);
        _gaq.push(['_setSiteSpeedSampleRate', 10]);
        _gaq.push(['_trackPageview']);

        (function() {
            var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
            ga.src = ('https:' == document.location.protocol ? 'https://' : 'http://') + 'stats.g.doubleclick.net/dc.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
        })();
    </script>



    <style>

        html, body {
            margin: 0;
            height: 100%;
            overflow-y: auto;
        }

        body {
            display: -webkit-flex;
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-align-items: center;
            -webkit-box-align: center;
                -ms-flex-align: center;
                    align-items: center;
        }

        a, a:active, a:visited, a:hover {
            color: #447ADB;
        }

        .page404 {
            margin: 0 auto;
            text-align: center;
            min-width: 260px;
            color: #333;
            padding: 24px;
        }

        .page404-heading {
            color: #447ADB;
            font-size: 100px;
            font-weight: 800;
            line-height: 100px;
        }

        .page404-bars {
            background-color: #447ADB;
            border-radius: 50%;
            box-sizing: border-box;
            display: inline-block;
            height: 75px;
            margin: 0 6px 10px 6px;
            padding-bottom: 20px;
            text-align: center;
            vertical-align: bottom;
            width: 75px;
        }

        .page404-bars svg {
            margin-bottom: 30px;
        }

        .page404-txt {
            font-weight: 300;
        }

        .page404-cta {
            padding: 24px 0;
        }

        .page404-cta p {
            margin: 0;
            line-height: 24px;
            line-height: 1.5rem;
        }

    </style>

</head>

<body>

    <div class="page404">
        <div class="page404-heading">
            4<div class="page404-bars">
                <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px"     y="0px" width="40px" height="40px" viewBox="0 0 304.128 246.216" enable-background="new 0 0 304.128 246.216"
                     xml:space="preserve">
                    <g>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M125.3,123.066c0,40.407-0.008,80.813,0.031,121.219
                                c0.001,1.588-0.347,1.932-1.57,1.926c-10.917-0.061-21.834-0.032-32.751-0.039c-1.731-0.001-1.558,0.249-1.558-1.894
                                c-0.003-80.813,0-161.625-0.026-242.438c0-1.378,0.196-1.848,1.408-1.841c11.037,0.065,22.074,0.058,33.111,0.009
                                c1.067-0.005,1.384,0.29,1.383,1.688C125.293,42.154,125.3,82.61,125.3,123.066z"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M214.786,140.75c0,34.522-0.008,69.046,0.027,103.568
                                c0.001,1.483-0.252,1.905-1.491,1.898c-11.078-0.068-22.156-0.065-33.234-0.001c-1.169,0.006-1.25-0.556-1.25-1.735
                                c0.019-69.244,0.02-138.49-0.007-207.734c0-1.291,0.222-1.676,1.307-1.67c11.118,0.055,22.236,0.055,33.354,0.001
                                c1.067-0.005,1.319,0.343,1.317,1.656C214.779,71.405,214.786,106.078,214.786,140.75z"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M134.18,158.268c0-28.739,0.007-57.477-0.022-86.215
                                c-0.001-1.324,0.222-1.744,1.353-1.738c11.079,0.058,22.158,0.052,33.237,0.006c1.006-0.004,1.25,0.337,1.25,1.574
                                c-0.025,57.576-0.025,115.151-0.001,172.728c0.001,1.222-0.225,1.588-1.241,1.582c-11.119-0.047-22.238-0.046-33.357,0
                                c-1.009,0.006-1.241-0.345-1.24-1.573C134.187,215.844,134.18,187.056,134.18,158.268z"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M223.665,193.287c0-16.962,0.013-33.925-0.024-50.887
                                c-0.003-1.355,0.265-1.732,1.372-1.726c11.079,0.054,22.157,0.051,33.235,0.001c1.022-0.003,1.234,0.365,1.233,1.583
                                c-0.026,34.125-0.026,68.25,0.001,102.375c0.001,1.229-0.23,1.579-1.24,1.573c-11.118-0.046-22.236-0.046-33.355,0
                                c-1.014,0.006-1.246-0.354-1.244-1.58C223.675,227.511,223.665,210.4,223.665,193.287z"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M44.694,211.117c0-11.222,0.018-22.443-0.024-33.663
                                c-0.004-1.296,0.228-1.672,1.31-1.667c11.114,0.054,22.229,0.048,33.343,0.005c1.004-0.003,1.27,0.352,1.269,1.588
                                c-0.028,22.442-0.028,44.885-0.001,67.327c0.001,1.176-0.252,1.501-1.2,1.496c-11.194-0.041-22.389-0.04-33.583-0.001
                                c-0.906,0.003-1.136-0.31-1.133-1.424C44.707,233.558,44.694,222.337,44.694,211.117z"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M286.165,246.176c-5.557,0-11.113-0.032-16.67,0.028
                                c-0.965,0.012-1.179-0.348-1.175-1.5c0.034-10.721,0.033-21.441,0.001-32.163c-0.003-1.128,0.183-1.516,1.165-1.511
                                c11.152,0.047,22.306,0.046,33.459,0.001c0.964-0.003,1.179,0.347,1.176,1.499c-0.035,10.721-0.042,21.442,0.007,32.162
                                c0.006,1.332-0.357,1.518-1.294,1.509C297.277,246.151,291.721,246.176,286.165,246.176z"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" fill="#FFF"
                              d="M17.89,246.176c-5.599,0-11.197-0.019-16.796,0.021
                                c-0.801,0.006-1.097-0.201-1.094-1.295c0.033-10.874,0.03-21.749,0.002-32.623c-0.002-1.002,0.248-1.24,1.016-1.238
                                c11.237,0.028,22.475,0.035,33.711-0.009c0.943-0.003,1.105,0.387,1.103,1.452c-0.029,10.774-0.033,21.55,0.004,32.324
                                c0.004,1.154-0.28,1.4-1.151,1.393C29.087,246.153,23.488,246.176,17.89,246.176z"/>
                    </g>
                </svg>
            </div>4
        </div>

        <div class="page404-txt">
            <h3>Plot twist!</h3>
            <h5>There's nothing here...</h5>

            <div class="page404-cta">
                <p>You might need to <a href="https://plot.ly/accounts/login" target="_blank">
                sign in</a> to see this plot.</p>

                <p><a href="https://plot.ly" target="_blank">Plotly</a> is free
                to view plots that have been shared with you.</p>
            </div>
        </div>
    </div>

</body>
</html>


