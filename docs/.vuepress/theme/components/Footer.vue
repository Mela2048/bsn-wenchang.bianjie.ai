<template>
    <div class="footer_content_wrapper">
        <div class="footer_content_top">
            <div class="top_content">
                <div class="content">
                    <div class="content_left">
                        <div class="left_img">
                            <a class="logo bsn_logo" href="https://bsnbase.com/" target="_blank" rel="noopener noreferrer">
                                <img
                                    src="../assets/bsn_logo.png"
                                    alt=""
                                />
                            </a>
                            <span class="line"></span>
                            <a class="logo irita_logo" href="https://irita.bianjie.ai/" target="_blank" rel="noopener noreferrer">
                                <img
                                    src="../assets/irita_logo.png"
                                    alt=""
                                />
                            </a>
                            <span class="line"></span>
                            <a class="logo bianjie_logo" href="https://www.bianjie.ai/" target="_blank" rel="noopener noreferrer">
                                <img
                                    src="../assets/bianjie_logo.png"
                                    alt=""
                                />
                            </a>
                        </div>
                        <p class="img_desc">
                            BSN 文昌链是基于 IRITA 打造，具备全生态商业服务能力的开放联盟链
                        </p>
                    </div>
                    <div class="content_right">
                        <div class="line"></div>
                        <div class="contact">
                            <span class="contact_title">联系我们</span>
                            <span class="email">contact@bianjie.ai</span>
                            <a
                                class="official"
                                href="https://www.bianjie.ai"
                                target="_blank"
                                rel="noopener noreferrer"
                                >www.bianjie.ai</a
                            >
                        </div>
                        <div class="focus">
                            <span class="focus_title">关注我们</span>
                            <span class="qr_code">
                                <img
                                    src="../assets/qrcode.png"
                                    alt=""
                                    class="qr_code_img"
                                />
                            </span>
                            <span class="desc">微信公众号 边界智能</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer_content_bottom">
            <div class="bottom_content">
                <span class="copyright_content">{{
                    `©${new Date().getFullYear()} All Rights Reserved`
                }}</span>
                <a
                    href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=31011502009028"
                    target="_blank"
                    rel="noreferrer noopener"
                    >沪ICP备17020986号</a
                >
                <span class="police_content">
                    <a
                        href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=31011502009028"
                        target="_blank"
                        rel="noreferrer noopener"
                        >沪公网安备31011502009028号</a
                    >
                </span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    methods: {
        toBSN() {
            window.open('https://www.bsnbase.com/');
        },
        toHome() {
            this.$router.push("/");
            this.$store.commit("currentIndex", 0);
        },
    }
};
</script>

<style lang="stylus">
.footer_content_wrapper {
    width: 100%;

    @media (max-width: 1030px) {
        margin-top: 0;
    }

    .footer_content_top {
        width: 100%;
        height: 31.4rem;
        background: #F9FAFD;

        @media (max-width: 1030px) {
            height: auto;
        }
    }

    .top_content {
        box-sizing: border-box;
        margin: 0 auto;
        padding: 6rem 4.8rem;
        max-width: $footerTopContentWidth;
        @media (max-width: 1030px) {
            padding: 6rem 1.6rem;
        }
        .content {
            display: flex;
            -webkit-box-pack: justify;
            -ms-flex-pack: justify;
            -webkit-justify-content: space-between;
            justify-content: space-between;
            @media (max-width: 1030px) {
                flex-direction: column;
                align-items: center;
            }
            .content_left {
                @media (max-width: 1030px) {
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                }
                .left_img {
                    display: flex;
                    align-items: center;
                    height: 4.8rem;
                    @media (max-width: 580px) {
                        flex-direction: column;
                        align-items: center;
                        height: auto;
                    }
                    .logo {
                        display: inline-block;
                        height: 4.8rem;
                        @media (max-width: 580px) {
                            margin-top: 1.6rem;
                            &:first-child {
                                margin-top: 0;
                            }
                        }
                        img {
                            height: 100%;
                            vertical-align: middle;
                        }
                    }
                    .line {
                        display: inline-block;
                        margin: 0 1.6rem;
                        width: 0.2rem;
                        height: 80%;
                        background: rgba(81, 80, 113, 0.15);
                        @media (max-width: 580px) {
                            display: none;
                        }
                    }
                }
                .img_desc {
                    margin-top: 2.4rem;
                    max-width: 54.7rem;
                    line-height: 2.4rem;
                    font-size: $fontSize16;
                    font-weight: $fontWeight400;
                    color: rgba(0, 0, 0, .75);
                    @media (max-width: 580px) {
                        text-align: center;
                    }
                }
            }
            .content_right {
                display: flex;
                -webkit-box-pack: justify;
                -ms-flex-pack: justify;
                -webkit-justify-content: space-between;
                justify-content: space-between;
                @media (max-width: 1030px) {
                    margin-top: 3.6rem;
                }
                @media (max-width: 580px) {
                    flex-direction: column;
                    align-items: center;
                }

                .line {
                    width: 0.1rem;
                    height: 19.5rem;
                    background: rgba(81, 80, 113, 0.15);
                    @media (max-width: 1030px) {
                        display: none;
                    }
                }

                .contact {
                    display: flex;
                    flex-direction: column;
                    -webkit-box-orient: vertical;
                    -ms-flex-direction: column;
                    -webkit-flex-direction: column;
                    margin: 0 8rem;
                    @media (max-width: 1030px) {
                        margin-left: 0;
                        text-align: center;
                    }
                    @media (max-width: 580px) {
                        margin-right: 0;
                    }

                    .contact_title {
                        height: 2.4rem;
                        line-height: 2.4rem;
                        font-size: $fontSize16;
                        font-weight: $fontWeight600;
                        color: #000;
                    }

                    .email {
                        margin: 2.4rem 0;
                        height: 2.4rem;
                        line-height: 2.4rem;
                        font-size: $fontSize16;
                        font-weight: $fontWeight400;
                        color: rgba(0, 0, 0, .75);

                        &:hover {
                            color: $highlightDetailColor;
                            cursor: pointer;
                        }
                    }

                    .official {
                        height: 2.4rem;
                        line-height: 2.4rem;
                        font-size: $fontSize16;
                        font-weight: $fontWeight400;
                        color: rgba(0, 0, 0, .75);

                        &:hover {
                            color: $highlightDetailColor;
                        }
                    }
                }

                .focus {
                    display: flex;
                    flex-direction: column;
                    @media (max-width: 1030px) {
                        text-align: center;
                    }
                    @media (max-width: 580px) {
                        margin-top: 2.4rem;
                    }

                    .focus_title {
                        line-height: 2.4rem;
                        font-size: $fontSize16;
                        font-weight: $fontWeight600;
                        color: #000;
                    }

                    .qr_code {
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        margin: 2.4rem 0 0.8rem;
                        width: 11.4rem;
                        height: 11.4rem;

                        .qr_code_img {
                            width: 11.4rem;
                            height: 11.4rem;
                            vertical-align: middle;
                        }
                    }

                    .desc {
                        line-height: 2.4rem;
                        font-size: $fontSize12;
                        font-weight: $fontWeight400;
                        color: rgba(0, 0, 0, .75);
                    }
                }
            }
        }
    }

    .footer_content_bottom {
        width: 100%;
        height: 6rem;
        font-size: $fontSize14;
        font-weight: $fontWeight400;
        background: $footerBottomColor;
        @media (max-width: 1200px) {
            box-sizing: border-box;
            padding-left: 4.8rem;
            padding-right: 4.8rem;
        }
    }

    .bottom_content {
        display: flex;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        -webkit-justify-content: space-between;
        justify-content: space-between;
        align-items: center;
        margin: 0 auto;
        max-width: 90rem;
        height: 100%;
        @media (max-width: 420px) {
            text-align: center;
        }

        .copyright_content {
            color: $whiteColorOpacity;
        }

        a {
            color: $whiteColorOpacity;
            cursor: pointer;
        }
    }
}

@media (max-width: 730px) {
    .footer_content_wrapper {
        .footer_content_bottom {
            height: auto;
            line-height: 3rem;

            .bottom_content {
                flex-direction: column;
            }
        }
    }
}
</style>
