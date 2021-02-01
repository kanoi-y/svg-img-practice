<template>
  <div class="container">
    <div class="wrap-svg">
      <svg
        id="svg"
        data-name="レイヤー 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 600 600"
        width="500"
        height="500"
      >
        <defs>
          <style>
            .cls-1 {
              fill: #c7b299;
            }
            .cls-1,
            .cls-2 {
              stroke: #000;
            }
            .cls-1,
            .cls-2,
            .cls-3 {
              stroke-miterlimit: 10;
            }
            .cls-3,
            .cls-4 {
              fill: #fff;
            }
            .cls-3 {
              stroke: #fff;
            }
            .cls-4 {
              font-size: 45px;
              font-family: KozGoPr6N-Regular-90ms-RKSJ-H, Kozuka Gothic Pr6N;
            }
          </style>
        </defs>
        <rect class="cls-1" x="0.5" y="2.5" width="600" height="596.27" />
        <polygon
          class="cls-2"
          points="440.88 599.88 161.51 599.88 259.01 288.78 405.26 288.78 440.88 599.88"
        />
        <path
          class="cls-2"
          d="M442.16,228l-56.91,95.82a8.92,8.92,0,0,1-9.56,4.16L266,304.13a8.92,8.92,0,0,1-7-7.83L248.16,187a8.92,8.92,0,0,1,6.49-9.47L374,144.44a8.9,8.9,0,0,1,9.26,2.92l58.12,70.42A8.93,8.93,0,0,1,442.16,228Z"
        />
        <path
          d="M320,219.59a11.21,11.21,0,0,1,8.6-15.39,1.52,1.52,0,0,0,1.05-1.85,1.54,1.54,0,0,0-1.85-1,14.47,14.47,0,0,0-9.59,6.58,14.24,14.24,0,0,0-1.1,12.5,1.55,1.55,0,0,0,1.85,1.05,1.51,1.51,0,0,0,1-1.85Z"
        />
        <ellipse
          class="cls-3"
          cx="332.68"
          cy="220.72"
          rx="20.46"
          ry="14.55"
          transform="translate(-39.55 76.37) rotate(-12.37)"
        />
        <path
          class="cls-2"
          d="M339.38,107.53l45.38,41.07a3,3,0,0,1-.68,5l-39.4,19.63a3,3,0,0,1-4.38-2.42l-6-60.7A3,3,0,0,1,339.38,107.53Z"
        />
        <path
          class="cls-2"
          d="M256.35,121.22l48.5,56a3,3,0,0,1-1.28,4.85L253.26,200a3,3,0,0,1-4-2.93l1.81-73.9A3,3,0,0,1,256.35,121.22Z"
        />
        <ellipse class="cls-2" cx="330.58" cy="221.14" rx="7.32" ry="12.93" />
        <path
          d="M381.92,195.37a11.41,11.41,0,0,1,.79-10.19,11.55,11.55,0,0,1,7.81-5.2,1.52,1.52,0,0,0,1-1.85,1.53,1.53,0,0,0-1.84-1,14.56,14.56,0,0,0-9.6,6.58A14.29,14.29,0,0,0,379,196.17a1.54,1.54,0,0,0,1.84,1.05,1.51,1.51,0,0,0,1.05-1.85Z"
        />
        <ellipse
          class="cls-3"
          cx="394.55"
          cy="196.5"
          rx="20.46"
          ry="14.55"
          transform="translate(-32.93 89.06) rotate(-12.37)"
        />
        <ellipse class="cls-2" cx="392.46" cy="196.92" rx="7.32" ry="12.93" />
        <polygon
          class="cls-2"
          points="448.91 175.59 415.17 213.65 417.86 215.48 451.59 177.42 448.91 175.59"
        />
        <polygon
          class="cls-2"
          points="467.13 197.61 423.84 224.48 425.88 227 469.17 200.13 467.13 197.61"
        />
        <path
          d="M189.37,561.72c-14.27-15.26-14-38.26-14.69-57.83q-.75-19.63-1.49-39.26c-.44-11.73.32-24.4-2.75-35.83-5.17-19.23-24.71-32.72-43.08-37.84-11.2-3.12-21.58-.78-30.85,6.07-8,5.93-16.94,13.29-19.12,23.56C74.83,432.68,81.73,441.9,93,445.45c9,2.81,19.24,8.92,27.72,2.15,6-4.81-2.51-13.25-8.49-8.48.32-.25-2.23-.6-3.07-.85-1.78-.53-3.51-1.26-5.24-1.93-3.39-1.3-7.19-1.87-10.44-3.46-9-4.43-3.11-14.59,2-19.55,6.29-6.07,14.27-12.68,23.54-11.82,8.33.77,16.76,5.3,23.61,9.88,6.41,4.29,12.27,10.15,15.16,17.43C161.5,438,160.6,449,161,458.74c.76,20.1,1.11,40.27,2.38,60.34,1.15,18.4,4.51,37.2,17.53,51.13,5.29,5.65,13.76-2.85,8.49-8.49Z"
        />
        <text class="cls-4" transform="translate(115.79 385.75)">
          これはテストです
        </text>
      </svg>
    </div>
    <button @click="createImg">画像を生成</button>
    <img id="img" src="" alt="" />
  </div>
</template>

<script>
export default {
  methods: {
    svg2jpeg(svgElement, sucessCallback, errorCallback) {
      const canvas = document.createElement("canvas");
      canvas.width = svgElement.width.baseVal.value;
      canvas.height = svgElement.height.baseVal.value;
      const ctx = canvas.getContext("2d");
      const image = new Image();

      // SVGデータを取り出す
      image.onload = () => {
        // SVGデータをPNG形式に変換する
        ctx.drawImage(image, 0, 0, image.width, image.height);
        sucessCallback(canvas.toDataURL());
      };
      image.onerror = e => {
        errorCallback(e);
      };
      const svgData = new XMLSerializer().serializeToString(svgElement);
      image.src =
        "data:image/svg+xml;charset=utf-8;base64," +
        btoa(unescape(encodeURIComponent(svgData)));
    },
    createImg() {
      if (process.client) {
        const svg = document.getElementById("svg");

        const sucessFunc = data => {
          console.log(data);
          document.getElementById("img").src = data;
        };

        const errorFunc = error => {
          console.error(error);
        };

        this.svg2jpeg(svg, sucessFunc, errorFunc);
      }
    }
  }
};
</script>

<style>
.container {
  text-align: center;
}
.wrap-svg {
  display: inline-flex;
  justify-content: center;
  width: 100%;
  padding-top: 50px;
  margin-bottom: 40px;
}

#svg {
  width: 500px;
}
</style>
