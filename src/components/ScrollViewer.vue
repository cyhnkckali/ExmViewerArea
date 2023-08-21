<!-- eslint-disable no-useless-escape -->
<template>
  <VueInfiniteViewer
    id="ck-main"
    :displayHorizontalScroll="false"
    :displayVerticalScroll="false"
    class="viewer card card-screen-block"
    ref="InfiniteViewer"
    :usePinch="true"
    :useMouseDrag="mouseDrag"
    :useWheelScroll="false"
    :useAutoZoom="true"
    :zoomRange="zoomRange"
    :maxPinchWheel="10"
    :rangeX="rangeX"
    :rangeY="rangeY"
    @pinch="onPinchInfiniteView"
    @scroll="onScrollInfiniteView"
    @dragStart="onDragStartInfiniteView"
  >
    <div class="viewport">
      <div
        id="ck-main-layout"
        style="
          position: relative;
          border-radius: 5px;
          left: 20px;
          top: 0px;
          width: 2000px;
          height: 3000px;
          z-index: 0;
          display: block;
        "
      >
        <div
          id="akf6"
          style="position: relative; left: 20px; top: 20px; z-index: 1"
          fornax-tag="I_akf6_Cooling_Loaded_Charge,I_akf6_Loaded_Charge"
        >
          <a clask="/Furnace/Index/1" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf6_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 6</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf6_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf6_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf6_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf6_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf6_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf6_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf6_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf6_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf6_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf6_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf6_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf6_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf6_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf6_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf8"
          style="position: relative; left: 370px; top: 20px; z-index: 1"
          fornax-tag="I_akf8_Cooling_Loaded_Charge,I_akf8_Loaded_Charge"
        >
          <a clask="/Furnace/Index/2" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf8_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 8</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf8_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf8_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf8_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf8_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf8_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf8_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf8_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf8_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf8_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf8_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf8_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf8_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf8_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf8_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv13"
          style="position: relative; left: 720px; top: 20px; z-index: 1"
          fornax-tag="I_mnv13_Loaded_Charge"
        >
          <a clask="/Furnace/Index/3" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv13_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 13</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv13_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv13_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv13_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv13_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv13_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv13_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv13_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv14"
          style="position: relative; left: 1070px; top: 20px; z-index: 1"
          fornax-tag="I_mnv14_Loaded_Charge"
        >
          <a clask="/Furnace/Index/4" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv14_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 14</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 367px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv14_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 367px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv14_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv14_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 196px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv14_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv14_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv14_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv14_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="ayf"
          style="position: relative; left: 1420px; top: 20px; z-index: 1"
          fornax-tag="I_ayf_Cooling_Loaded_Charge,I_ayf_Loaded_Charge"
        >
          <a clask="/Furnace/Index/5" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="ayf_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AYF</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AYF.png"
              style="
                top: 65px;
                left: 10px;
                width: 206px;
                height: 300px;
                position: absolute;
                z-index: 2;
                transform: rotate(180deg);
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="ayf_firin_sck_set|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="ayf_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="ayf_sepet_yag|visible"
              style="
                position: absolute;
                left: 35px;
                top: 197px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayf_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayf_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayf_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="ayf_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="ayf_sepet|visible"
              style="
                position: absolute;
                left: 35px;
                top: 65px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayf_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayf_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayf_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="ayf_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf3"
          style="position: relative; left: 20px; top: 500px; z-index: 1"
          fornax-tag="I_akf3_Cooling_Loaded_Charge,I_akf3_Loaded_Charge"
        >
          <a clask="/Furnace/Index/6" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf3_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 3</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf3_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf3_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf3_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf3_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf3_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf3_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf3_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf3_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf3_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf3_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf3_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf3_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf3_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf3_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv1"
          style="position: relative; left: 370px; top: 500px; z-index: 1"
          fornax-tag="I_mnv1_Loaded_Charge"
        >
          <a clask="/Furnace/Index/7" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv1_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 1</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv1_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv1_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv1_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv1_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv1_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv1_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv1_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv2"
          style="position: relative; left: 720px; top: 500px; z-index: 1"
          fornax-tag="I_mnv2_Loaded_Charge"
        >
          <a clask="/Furnace/Index/8" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv2_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 2</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv2_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv2_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv2_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv2_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv2_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv2_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv2_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv3"
          style="position: relative; left: 1070px; top: 500px; z-index: 1"
          fornax-tag="I_mnv3_Loaded_Charge"
        >
          <a clask="/Furnace/Index/9" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv3_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 3</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv3_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv3_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv3_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv3_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv3_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv3_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv3_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="vm43"
          style="position: relative; left: 1420px; top: 500px; z-index: 1"
          fornax-tag="I_vm43_Loaded_Charge"
        >
          <a clask="/Furnace/Index/10" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="vm43_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >VM 43</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="vm43_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="vm43_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="vm43_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="vm43_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="vm43_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="vm43_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="vm43_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv10"
          style="position: relative; left: 20px; top: 980px; z-index: 1"
          fornax-tag="I_mnv10_Loaded_Charge"
        >
          <a clask="/Furnace/Index/11" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv10_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 10</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv10_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv10_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv10_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv10_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv10_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv10_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv10_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="ayfm1"
          style="position: relative; left: 370px; top: 980px; z-index: 1"
          fornax-tag="I_ayfm1_Loaded_Charge"
        >
          <a clask="/Furnace/Index/12" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="ayfm1_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AYFM 1</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="ayfm1_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="ayfm1_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="ayfm1_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayfm1_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayfm1_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayfm1_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="ayfm1_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv8"
          style="position: relative; left: 720px; top: 980px; z-index: 1"
          fornax-tag="I_mnv8_Loaded_Charge"
        >
          <a clask="/Furnace/Index/13" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv8_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 8</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv8_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv8_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv8_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv8_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv8_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv8_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv8_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv9"
          style="position: relative; left: 1070px; top: 980px; z-index: 1"
          fornax-tag="I_mnv9_Loaded_Charge"
        >
          <a clask="/Furnace/Index/14" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv9_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 9</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv9_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv9_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv9_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv9_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv9_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv9_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv9_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv5"
          style="position: relative; left: 1420px; top: 980px; z-index: 1"
          fornax-tag="I_mnv5_Loaded_Charge"
        >
          <a clask="/Furnace/Index/15" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv5_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 5</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv5_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv5_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv5_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv5_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv5_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv5_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv5_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf2"
          style="position: relative; left: 20px; top: 1460px; z-index: 1"
          fornax-tag="I_akf2_Cooling_Loaded_Charge,I_akf2_Loaded_Charge"
        >
          <a clask="/Furnace/Index/16" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf2_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 2</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf2_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf2_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf2_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf2_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf2_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf2_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf2_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf2_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf2_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf2_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf2_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf2_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf2_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf2_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="emnv11"
          style="position: relative; left: 370px; top: 1460px; z-index: 1"
          fornax-tag="I_emnv11_Loaded_Charge"
        >
          <a clask="/Furnace/Index/17" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="emnv11_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 11</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="emnv11_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="emnv11_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="emnv11_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="emnv11_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="emnv11_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="emnv11_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="emnv11_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv12"
          style="position: relative; left: 720px; top: 1460px; z-index: 1"
          fornax-tag="I_mnv12_Loaded_Charge"
        >
          <a clask="/Furnace/Index/18" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv12_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 12</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv12_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv12_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv12_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv12_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv12_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv12_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv12_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv4"
          style="position: relative; left: 1070px; top: 1460px; z-index: 1"
          fornax-tag="I_mnv4_Loaded_Charge"
        >
          <a clask="/Furnace/Index/19" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv4_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 4</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv4_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv4_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv4_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv4_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv4_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv4_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv4_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf1"
          style="position: relative; left: 1420px; top: 1460px; z-index: 1"
          fornax-tag="I_akf1_Cooling_Loaded_Charge,I_akf1_Loaded_Charge"
        >
          <a clask="/Furnace/Index/20" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf1_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 1</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf1_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf1_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf1_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf1_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf1_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf1_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf1_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf1_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf1_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf1_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf1_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf1_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf1_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf1_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="vf1"
          style="position: relative; left: 20px; top: 1940px; z-index: 1"
          fornax-tag="I_vf1_Loaded_Charge"
        >
          <a clask="/Furnace/Index/21" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="vf1_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >VF 1</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/VF.png"
              style="
                top: 68px;
                left: 10px;
                width: 188px;
                height: 278px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Fırın Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="0"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="vf1_analoginput_firin_knt_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Fırın Vakum</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="mBar"
                  digit="0"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="vf1_analoginput_cmb_vkm_1|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Fırın Basınç</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="bar"
                  digit="2"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="vf1_analoginput_firin_basinc_1|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
                display: none;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="vf1_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="vf1_Program_running|visible"
              style="
                position: absolute;
                left: 32px;
                top: 110px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="vf1_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="vf1_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="vf1_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="vf1_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv6"
          style="position: relative; left: 370px; top: 1940px; z-index: 1"
          fornax-tag="I_mnv6_Loaded_Charge"
        >
          <a clask="/Furnace/Index/22" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv6_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 6</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv6_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv6_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv6_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv6_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv6_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv6_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv6_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="ayfm2"
          style="position: relative; left: 720px; top: 1940px; z-index: 1"
          fornax-tag="I_ayfm2_Loaded_Charge"
        >
          <a clask="/Furnace/Index/23" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="ayfm2_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AYFM 2</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="ayfm2_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="ayfm2_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="ayfm2_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayfm2_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayfm2_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="ayfm2_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="ayfm2_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="mnv7"
          style="position: relative; left: 1070px; top: 1940px; z-index: 1"
          fornax-tag="I_mnv7_Loaded_Charge"
        >
          <a clask="/Furnace/Index/24" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="mnv7_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >MNV 7</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/MNV.png"
              style="
                top: 192px;
                left: 10px;
                width: 207px;
                height: 173px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv7_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="mnv7_proses_sck_deger|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="mnv7_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv7_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv7_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="mnv7_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="mnv7_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf5"
          style="position: relative; left: 1420px; top: 1940px; z-index: 1"
          fornax-tag="I_akf5_Cooling_Loaded_Charge,I_akf5_Loaded_Charge"
        >
          <a clask="/Furnace/Index/25" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf5_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 5</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf5_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf5_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf5_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf5_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf5_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf5_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf5_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf5_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf5_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf5_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf5_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf5_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf5_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf5_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf4"
          style="position: relative; left: 20px; top: 2420px; z-index: 1"
          fornax-tag="I_akf4_Cooling_Loaded_Charge,I_akf4_Loaded_Charge"
        >
          <a clask="/Furnace/Index/26" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf4_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 4</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf4_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf4_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf4_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf4_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf4_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf4_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf4_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf4_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf4_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf4_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf4_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf4_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf4_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf4_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>

        <div
          id="akf7"
          style="position: relative; left: 370px; top: 2420px; z-index: 1"
          fornax-tag="I_akf7_Cooling_Loaded_Charge,I_akf7_Loaded_Charge"
        >
          <a clask="/Furnace/Index/27" style="color: #3f4254">
            <div style="top: 10px; left: 71px; position: absolute; z-index: 2">
              <div
                class="d-flex align-items-center bg-gray-500 rounded p-2"
                fornax-tag="akf7_Program_running|running"
              >
                <span class="svg-icon svg-icon-white svg-icon-2x">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink"
                    width="24px"
                    height="24px"
                    viewBox="0 0 24 24"
                    version="1.1"
                  >
                    <g
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <rect x="0" y="0" width="24" height="24"></rect>
                      <path
                        d="M7.62302337,5.30262097 C8.08508802,5.000107 8.70490146,5.12944838 9.00741543,5.59151303 C9.3099294,6.05357769 9.18058801,6.67339112 8.71852336,6.97590509 C7.03468892,8.07831239 6,9.95030239 6,12 C6,15.3137085 8.6862915,18 12,18 C15.3137085,18 18,15.3137085 18,12 C18,9.99549229 17.0108275,8.15969002 15.3875704,7.04698597 C14.9320347,6.73472706 14.8158858,6.11230651 15.1281448,5.65677076 C15.4404037,5.20123501 16.0628242,5.08508618 16.51836,5.39734508 C18.6800181,6.87911023 20,9.32886071 20,12 C20,16.418278 16.418278,20 12,20 C7.581722,20 4,16.418278 4,12 C4,9.26852332 5.38056879,6.77075716 7.62302337,5.30262097 Z"
                        fill="#000000"
                        fill-rule="nonzero"
                      ></path>
                      <rect
                        fill="#000000"
                        x="11"
                        y="3"
                        width="2"
                        height="10"
                        rx="1"
                      ></rect>
                    </g>
                  </svg>
                </span>

                <div class="d-flex flex-column flex-grow-1 mr-2">
                  <span class="font-weight-bold text-white font-size-lg"
                    >AKF 7</span
                  >
                </div>
              </div>
            </div>
            <img
              id="imgZemin"
              src="/media/Tesis/AKF.png"
              style="
                top: 89px;
                left: 10px;
                width: 206px;
                height: 276px;
                position: absolute;
                z-index: 2;
              "
            />
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Set Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf7_program_anlik_set_sicakligi|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 364px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel Sıcaklık</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf7_firin_sck|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 10px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm">Set CP</span>
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf7_program_step_anlik_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              style="
                min-width: 100px;
                position: absolute;
                left: 117px;
                top: 414px;
                z-index: 47;
              "
            >
              <span class="d-block font-weight-bold font-size-sm"
                >Aktuel CP</span
              >
              <span
                class="d-block text-center bg-secondary btn-sm font-weight-bold font-size-h6"
              >
                <span
                  class="text"
                  unit="°C"
                  digit="1"
                  min="-9999"
                  max="9999"
                  style="color: #1bc5bd"
                  fornax-tag="akf7_firin_cp|write;text"
                  >10</span
                >
              </span>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf7_sepet_yag|visible"
              style="
                position: absolute;
                left: 40px;
                top: 61px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf7_sg_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf7_sg_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf7_sg_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf7_sg_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
            <div
              class="bg-warning"
              fornax-tag="akf7_sepet|visible"
              style="
                position: absolute;
                left: 40px;
                top: 193px;
                z-index: 3;
                width: 150px;
                height: 185px;
                transform: scale(0.57);
              "
            >
              <div class="py-2 px-2">
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Şarj No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf7_program_charge_no"
                    style="color: white"
                    >0</span
                  >
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">AMS Load No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf7_program_ams_load_no"
                    style="color: white"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete Adı:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1 border-bottom"
                >
                  <span
                    class="text"
                    id="akf7_program_recipe_Name"
                    style="color: white; white-space: nowrap; overflow: hidden"
                  ></span>
                </div>

                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span class="font-weight-bold mr-3">Reçete No:</span>
                </div>
                <div
                  class="d-flex align-items-center font-weight-bold justify-content-between mb-1"
                >
                  <span
                    class="text"
                    id="akf7_program_recipe_code"
                    style="color: white"
                  ></span>
                </div>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </VueInfiniteViewer>
</template>
<script setup>
import { onMounted, ref } from "vue";
import { VueInfiniteViewer } from "vue3-infinite-viewer";

const zoomRange = ref([0.1, 100]);
const rangeX = ref([0, 0]);
const rangeY = ref([0, 0]);
const mouseDrag = ref(false);

// InfiniteView Scroll Methot
const InfiniteViewer = ref(null);

let widthMinZoom;
let heightMinZoom;
let sonuc;

const calculeteFirstSettingValue = () => {
  try {
    mouseDrag.value = false;
    let main = document.querySelector("#ck-main");
    let layout = document.querySelector("#ck-main-layout");

    let mWidth = main.offsetWidth;
    let mHeight = main.offsetHeight;
    let lWidth = layout.offsetWidth;
    let lHeight = layout.offsetHeight;

    let wRatio = lWidth / mWidth;
    let hRatio = lHeight / mHeight;

    let wScaleRatio = 100 / wRatio / 100;
    let hScaleRatio = 100 / hRatio / 100;

    widthMinZoom = wScaleRatio;
    heightMinZoom = hScaleRatio;
    rangeX.value = [0, 0];
    rangeY.value = [0, 0];

    sonuc = wScaleRatio >= hScaleRatio ? hScaleRatio : wScaleRatio;

    zoomRange.value = [sonuc, 1];

    setTimeout(() => {
      InfiniteViewer.value.setZoom([sonuc, sonuc]);
      setCenter((mWidth - lWidth * sonuc) / 2);
    });
  } catch (error) {
    /* empty */
  }
};

const setCenter = (left) => {
  try {
    const input = document.querySelector(".viewport");
    const regex = /(translate3d\(.*?\))\s*(scale\(.*?\))/;
    const matches = input.style.transform.match(regex);
    const [, , scale] = matches;

    if (left) {
      document.querySelector(
        ".viewport"
      ).style.transform = `translate3d(${left}px, 0px, 0px) ${scale}`;
    } else {
      let main = document.querySelector("#ck-main");
      let layout = document.querySelector("#ck-main-layout");

      let mWidth = main.offsetWidth;
      let lWidth = layout.offsetWidth;
      let mHeight = main.offsetHeight;
      let lHeight = layout.offsetHeight;

      let zoomValue = InfiniteViewer.value.getZoom();

      if (mHeight < lHeight * zoomValue) {
        let rY = lHeight * zoomValue - mHeight;

        rangeY.value = [0, rY];
      } else {
        rangeY.value = [0, 0];
      }
      if (mWidth < lWidth * zoomValue) {
        let rX = lWidth * zoomValue - mWidth;

        rangeX.value = [0, rX];
      } else {
        rangeX.value = [0, 0];
      }

      if (mHeight >= lHeight * zoomValue && mWidth >= lWidth * zoomValue) {
        mouseDrag.value = false;
      } else {
        mouseDrag.value = true;
      }

      if (mWidth >= lWidth * zoomValue) {
        let value = (mWidth - lWidth * zoomValue) / 2;
        // eslint-disable-next-line no-useless-escape

        let viewport = InfiniteViewer.value.getViewport();

        const vRegex = /translate3d\((.*?)\) scale\((.*?)\)/;

        const vMatches = viewport.style.transform.match(vRegex);

        const xyzValues = vMatches[1].split(",");
        const scaleValue = vMatches[2];

        setTimeout(() => {
          viewport.style.transform = `translate3d(${value}px, ${xyzValues[1]}, ${xyzValues[2]}) scale(${scaleValue})`;
        }, 1);
      }
    }
  } catch (error) {
    console.log(error);
  }
};

const onPinchInfiniteView = (e) => {
  if (heightMinZoom >= widthMinZoom && e.zoomX < widthMinZoom) {
    InfiniteViewer.value.setZoom([sonuc, sonuc]);
    rangeX.value = [0, 0];
  } else if (e.zoomY < heightMinZoom) {
    InfiniteViewer.value.setZoom([sonuc, sonuc]);
    rangeY.value = [0, 0];
  }
  setCenter();
};

const onScrollInfiniteView = (e) => {
  setCenter();
};

const onDragStartInfiniteView = (e) => {
  setCenter();
};

onMounted(() => {
  console.log(InfiniteViewer.value);

  calculeteFirstSettingValue();

  window.addEventListener("resize", (e) => {
    "ceyhun";
    calculeteFirstSettingValue();
  });
});
</script>

<style>
.viewer {
  box-sizing: border-box;
  width: 100vw;
  height: 100vh;
  user-select: none;
}

.viewport {
  width: 100%;
  height: 100%;
}

.row {
  position: relative;
  width: 100%;
  height: 100%;
}
</style>
