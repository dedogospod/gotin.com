<template>
  <div class="position-relative">
    <div class="row center-xs">
        <div class="avatar" :style="{ 'background-image': 'url(' + user.avatar + ')' }">
        </div>
    </div>
    <div class="row gotin-si-wrap">
        <div class="row row--no-margin center-xs gotin-si-cont">
            <div class="gotin-si-button">ГОТИН СИ!</div>
        </div>
    </div>
    <div class="row info">
        <div class="column col-xs-12">
            <div class="row center-xs username">
                {{user.displayName}}
            </div>
            <div class="row center-xs title">{{user.title}}</div>
            <div class="row">
                <div class="col-xs-6">
                    <div class="row center-xs upvotes">{{user.gotinCount}} </div>
                    <div class="row center-xs">
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="32" height="32" viewBox="0 0 128 128">
                            <path d=" M5.44,45.69c33.94-5,39.99,1.27,58.7,1.65c18.71-0.38,24.76-7.65,58.7-1.65c2.12,0.38,2.33,0.47,2.69,2.57 c0.15,0.93,0.25,4.86,0.28,5.79c0.07,1.72-0.27,1.95-1.98,2.86c-1.49,0.79-2.18,1.02-2.18,4.16c0,20.7-9.4,27.1-22.03,27.59 c-13.35,0.52-24.21-7.07-28.73-18.72c-6.4-16.46-7.4-16.47-13.8,0C52.58,81.59,42,89.19,28.66,88.67 c-12.63-0.5-22.03-7.64-22.03-27.59c0-3.14-0.69-3.37-2.18-4.16C2.74,56,2.39,55.77,2.47,54.05c0.04-0.93,0.14-4.86,0.28-5.79 C3.11,46.16,3.32,47.06,5.44,45.69L5.44,45.69z" style="fill-rule:evenodd;clip-rule:evenodd;fill:#2F2F2F;stroke:#464747;stroke-width:3;stroke-miterlimit:10;"/>
                            <g>
                                <path d="M115.23,60.04L115.23,60.04c0.17-7.79-0.93-9.6-5.87-10.61 c-4.63-0.95-9.37-1.41-14.05-1.23c-5.63,0.22-12.03,2.41-16.36,4.34c-5.52,2.47-6.31,2.94-5.11,6.43 c3.39,9.86,7.62,23.24,24.76,22.61C111.28,81.1,114.97,72.04,115.23,60.04" style="fill-rule:evenodd;clip-rule:evenodd;fill:#FFFFFF;"/>
                                <path d="M11.79,60.04c0.27,12,3.95,21.07,16.63,21.53 c17.15,0.64,21.37-12.75,24.76-22.61c1.2-3.49,0.41-3.96-5.11-6.43c-4.32-1.93-10.72-4.12-16.36-4.34 c-4.68-0.18-9.42,0.28-14.05,1.23C12.71,50.44,11.61,52.25,11.79,60.04z" style="fill-rule:evenodd;clip-rule:evenodd;fill:#FFFFFF;"/>
                                <path d="M5.44,45.69c33.94-5,39.99,1.27,58.7,1.65 c18.71-0.38,24.76-7.65,58.7-1.65c2.12,0.38,2.33,0.47,2.69,2.57c0.15,0.93,0.25,4.86,0.28,5.79c0.07,1.72-0.27,1.95-1.98,2.86 c-1.49,0.79-2.18,1.02-2.18,4.16c0,20.7-9.4,27.1-22.03,27.59c-13.35,0.52-24.21-7.07-28.73-18.72c-6.4-16.46-7.4-16.47-13.8,0 C52.58,81.59,42,89.19,28.66,88.67c-12.63-0.5-22.03-7.64-22.03-27.59c0-3.14-0.69-3.37-2.18-4.16C2.74,56,2.39,55.77,2.47,54.05 c0.04-0.93,0.14-4.86,0.28-5.79C3.11,46.16,3.32,47.06,5.44,45.69L5.44,45.69z M116.08,60.68c0.17-7.79-0.93-9.6-5.87-10.61 c-4.63-0.95-9.37-1.41-14.05-1.23c-5.63,0.22-12.07,1.44-16.39,3.37c-5.52,2.47-6.13,4.4-4.93,7.88 c3.39,9.86,7.46,22.76,24.61,22.12C112.13,81.74,115.82,72.68,116.08,60.68L116.08,60.68z M12.2,60.68 c0.27,12,3.95,21.07,16.63,21.53C45.98,82.84,50.2,69.46,53.59,59.6c1.2-3.49,0.41-3.96-5.11-6.43 c-4.32-1.93-10.72-4.12-16.36-4.34c-4.68-0.18-9.42,0.28-14.05,1.23C13.13,51.08,12.03,52.89,12.2,60.68z" style="fill-rule:evenodd;clip-rule:evenodd;fill:#2F2F2F;"/>
                                <path d="M54.15,69.53C49.55,77.87,37.89,85.3,30,85.3c-7.89,0-18.83-4.73-16.26-17.32 c2.71-13.3,8.37-19.82,16.26-19.82C37.89,48.15,65.32,49.25,54.15,69.53z" style="fill:#2F2F2F;"/>
                                <path d="M118.31,69.53c-3.72,8.77-16.25,15.77-24.15,15.77s-14.61-7.2-14.39-18.31 c0.25-12.32,7.65-18.97,15.54-18.79C110.98,48.55,127.08,48.83,118.31,69.53z" style="fill:#2F2F2F;"/>
                            </g>
                        </svg>
                    </div>
                </div>
                <div class="col-xs-6">
                    <div class="upvotes text-center">
                        <span class="ti-email"></span>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'UserProfile',
  props: ['user']
}
</script>
<style lang="scss" scoped>
    @import '../../assets/styles/settings/colors';
    @import '../../assets/styles/settings/variables';

    .avatar {
        background: no-repeat center center;
        min-height: 200px;
        width: 100%;
        background-size: cover;
    }

    .gotin-si {
        &-wrap {
            position: relative;
            border: 2px solid $themeGreen;
        }

        &-cont {
            position: absolute;
            top: -22px;
            width: 100%;
        }

        &-button {
            font-size: 24px;
            color: white;
            background: $themeGreen;
            padding: 10px 20px 4px;
            border-radius: 8px;
            text-align: center;
            cursor: pointer;
            font-family: $fontLogo;
        }
    }

    .info {
        background: primaryBackgroundColor;
        padding: 30px 15px;
        border: 1px solid $themeGreen;
    }

    .username {
        font-size: 18px;
    }

    .title {
        font-size: 12px;
        font-weight: bold;
        margin-bottom: 30px;
        opacity: 0.6;
    }

    .upvotes {
        font-size: 36px;
    }
</style>
